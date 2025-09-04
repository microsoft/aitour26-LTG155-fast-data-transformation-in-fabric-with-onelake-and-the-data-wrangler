<p align="center">
<img src="img/Banner-MS-AI-Tour-26.png" alt="decorative banner" width="1200"/>
</p>

# [Microsoft AI Tour 2026](https://aitour.microsoft.com)

## ⚡️ LTG155: Fast data transformation in Fabric with OneLake and the Data Wrangler

If you are delivering this session, review the [docs](./docs/) folder for step-by-step Microsoft Fabric demo setup and effective delivery guidance.

### Session Description

Prepping data shouldn’t feel like a chore. See how multi-cloud OneLake shortcuts connect to data sources without duplication, run shortcut file transforms and shortcut AI transforms like summarization and PII detection, and use Data Wrangler to clean and shape results, inside Microsoft Fabric.

### 🧠 Learning Outcomes

By the end of this lightning talk, attendees will:

- Understand how OneLake Shortcuts can unify data across clouds without duplication or movement.
- See how shortcut AI transformations (like sentiment analysis and PII detection) can enrich raw data instantly.
- Learn how to use Data Wrangler and Copilot to clean and shape data interactively, with AI-assisted suggestions and code generation.
- Walk away with a practical, reproducible workflow for preparing AI-ready data in Microsoft Fabric.

### 💻 Technologies Used

1. Microsoft Fabric
1. Microsoft Dataverse
1. Azure Storage

### 🔗 Session Resources

| Resources                             | Links                                                                                       | Description                    |
| :------------------------------------ | :------------------------------------------------------------------------------------------ | :----------------------------- |
| Additional Resources for this session | [https://learn.microsoft.com](https://learn.microsoft.com?ocid=AITour26_resourcecenter_cnl) | Links specific to this session |

### 📚 Continued Learning Resources

| Resources                          | Links                                                                                                                            | Description                                  |
| :--------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------- |
| AI Tour 2026 Resource Center       | [https://aka.ms/AITour26-Resource-Center](https://aka.ms/AITour26-Resource-Center?ocid=AITour26_resourcecenter_cnl)              | Links to all repos for AI Tour 26 Sessions   |
| Azure AI Foundry Community Discord | [![Microsoft Azure AI Foundry Discord](https://dcbadge.limes.pink/api/server/ByRwuEEgH4)](https://discord.com/invite/ByRwuEEgH4) | Connect with the Azure AI Foundry Community! |
| Learn at AI Tour                   | [https://aka.ms/LearnAtAITour](https://aka.ms/LearnAtAITour?ocid=AITour26_resourcecenter_cnl)                                    | Continue learning on Microsoft Learn         |

## View docs in your browser

This repo is configured to let you optionally browse the [documentation](./docs/) served locally with [MkDocs](https://www.mkdocs.org/).  

Please follow these steps to view the docs with MkDocs.

1. Install the `mkdocs-material` package
    ```bash
    pip install mkdocs-material
    ```

2. Run the `mkdocs serve` command from the root folder
    ```bash
    mkdocs serve
    ```
If you're running this repo in a GitHub Codespace, then you should be able to skip step 1.


## Content Owners

<table>
<tr>
    <td align="center"><a href="http://github.com/Jcardif">
        <img src="https://github.com/Jcardif.png" width="100px;" alt="Josh Ndemenge""/><br />
        <sub><b> Josh Ndemenge </b></sub></a><br />
            <a href="https://github.com/Jcardif" title="talk">📢</a> 
    </td>
    <td align="center"><a href="http://github.com/toolboc">
        <img src="https://github.com/toolboc.png" width="100px;" alt="Paul DeCarlo"/><br />
        <sub><b>Paul DeCarlo</b></sub></a><br />
            <a href="https://github.com/toolboc" title="talk">📢</a> 
    </td>
</tr></table>

## Responsible AI

Microsoft is committed to helping our customers use our AI products responsibly, sharing our learnings, and building trust-based partnerships through tools like Transparency Notes and Impact Assessments. Many of these resources can be found at [https://aka.ms/RAI](https://aka.ms/RAI).
Microsoft’s approach to responsible AI is grounded in our AI principles of fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability.

Large-scale natural language, image, and speech models - like the ones used in this sample - can potentially behave in ways that are unfair, unreliable, or offensive, in turn causing harms. Please consult the [Azure OpenAI service Transparency note](https://learn.microsoft.com/legal/cognitive-services/openai/transparency-note?tabs=text) to be informed about risks and limitations.

The recommended approach to mitigating these risks is to include a safety system in your architecture that can detect and prevent harmful behavior. [Azure AI Content Safety](https://learn.microsoft.com/azure/ai-services/content-safety/overview) provides an independent layer of protection, able to detect harmful user-generated and AI-generated content in applications and services. Azure AI Content Safety includes text and image APIs that allow you to detect material that is harmful. Within Azure AI Foundry portal, the Content Safety service allows you to view, explore and try out sample code for detecting harmful content across different modalities. The following [quickstart documentation](https://learn.microsoft.com/azure/ai-services/content-safety/quickstart-text?tabs=visual-studio%2Clinux&pivots=programming-language-rest) guides you through making requests to the service.

Another aspect to take into account is the overall application performance. With multi-modal and multi-models applications, we consider performance to mean that the system performs as you and your users expect, including not generating harmful outputs. It's important to assess the performance of your overall application using [Performance and Quality and Risk and Safety evaluators](https://learn.microsoft.com/azure/ai-studio/concepts/evaluation-metrics-built-in). You also have the ability to create and evaluate with [custom evaluators](https://learn.microsoft.com/azure/ai-studio/how-to/develop/evaluate-sdk#custom-evaluators).

You can evaluate your AI application in your development environment using the [Azure AI Evaluation SDK](https://microsoft.github.io/promptflow/index.html). Given either a test dataset or a target, your generative AI application generations are quantitatively measured with built-in evaluators or custom evaluators of your choice. To get started with the azure ai evaluation sdk to evaluate your system, you can follow the [quickstart guide](https://learn.microsoft.com/azure/ai-studio/how-to/develop/flow-evaluate-sdk). Once you execute an evaluation run, you can [visualize the results in Azure AI Foundry portal ](https://learn.microsoft.com/azure/ai-studio/how-to/evaluate-flow-results).
