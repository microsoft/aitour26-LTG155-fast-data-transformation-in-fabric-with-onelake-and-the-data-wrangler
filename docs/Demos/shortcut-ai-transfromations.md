# Demo 3 - Shortcut AI Transformations

This demo showcases how easy it is to create a transformed shortcut in OneLake using built-in AI capabilities for unstructured text. The focus is on applying AI-powered PII detection and redaction to chat transcript `.txt` files stored in Azure Blob Storage—automatically and dynamically—just like the file-based shortcut transformations in the previous demo.

## Pre-Requisites

1. An Azure Storage Account provisioned on Azure with the following container:

    - `support-chats-export`

1. Upload all the chat transcript `.txt` files from the [`data/chats/az-storage`](/data/chats/az-storage) folder to the `support-chats-export` container.
1. In the same Fabric workspace used in the previous demos, continue with the existing lakehouse: `StoreOps_Bronze_LH` (Lakehouse Schema enabled).

## Steps

1. Open the `StoreOps_Bronze_LH` lakehouse and switch to the **Files** tab in the Lakehouse explorer.
1. Create a new shortcut by selecting **New shortcut** (or right-clicking in the Files Folder) and choose **Azure Blob Storage** as the external source.
1. Select the existing connection to the Azure Storage Account and select the `support-chats-export` container that contains the uploaded multilingual chat transcript `.txt` files. Select **Next**.
1. In the shortcut transformation pane, select the **PII detection** option (other options like translation or summarization may also be available, but we will focus on PII redaction for this demo). Proceed to the next step.
1. Provide a meaningful name for the shortcut and select **Create** to start the AI-powered transformation process.
1. Once creation begins, use the notification card to select **Manage shortcut** and monitor progress. Wait until the status shows **Success** for the AI transformation.
1. After completion, open the shortcut in the Files explorer and browse the redacted chat transcript files. Open one of the English transcripts and verify that sensitive entities (emails, phone numbers, payment details) have been redacted.
1. Open a transcript in another language (e.g., one of the German `chat_DE_*.txt` files) and verify that PII has also been successfully detected and redacted across languages.
1. To demonstrate the dynamic behavior, upload the  files: *[chat_EN_5b969b81-aa85-45ed-bbd6-ac0a3294db9a.txt](/data/chats/chat_EN_5b969b81-aa85-45ed-bbd6-ac0a3294db9a.txt)* and [chat_ES_dd3f413e-a414-4d80-b220-081acc09ce2a.txt](/data/chats/chat_ES_dd3f413e-a414-4d80-b220-081acc09ce2a.txt)* in the `support-chats-export` container using the Azure Portal or Azure Storage Explorer.
1. Return to Fabric, right-click the shortcut, and select **Manage shortcut** to observe that Fabric automatically detects the file changes and triggers an incremental AI transformation—no manual refresh or pipelines required.
1. Refresh the shortcut contents. Confirm the newly added files appear with PII already redacted (and removed files no longer appear if any were deleted), validating continuous compliance.

Notice that the AI transformation keeps the redacted view synchronized with the container contents—new, changed, or removed files are reflected automatically without additional orchestration.

A complete recording can be found on slide 9 of the [powerpoint presentation](https://aka.ms/AAxubxj).
