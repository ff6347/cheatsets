---
title: Interpret web pages
source: https://help.obsidian.md/web-clipper/interpreter
author:
  - "[[Obsidian Help]]"
published:
created: 2025-05-28
description: Interpret web pages - Obsidian Help
tags:
  - cheatsets
---
Summary: 

---

Interpreter is a [Web Clipper](https://help.obsidian.md/web-clipper) feature that lets you interact with web pages using natural language. Interpreter helps you capture and modify data that you want to save to Obsidian. For example:

- Extract specific text fragments.
- Summarize or explain information.
- Convert text from one format to another.
- Translate text to a different language.

Interpreter leverages language models to process information on a web page, and return results using [Variables](https://help.obsidian.md/web-clipper/variables) that you can add to your [Web Clipper Templates](https://help.obsidian.md/web-clipper/templates).

<video controls="" src="https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/Attachments/video/web-clipper-interpreter-demo.mp4#t=0.001"></video>

## Examples of prompts

Prompts use the [variable](https://help.obsidian.md/web-clipper/variables) syntax `{{"your prompt"}}`. You can use this syntax with any natural language query, e.g.

- `{{"a summary of the page"}}` to extract a summary of the page.
- `{{"a three bullet point summary, translated to French"}}` to extract bullet points about the page, and translate them to French.
- `{{"un resumé de la page en trois points"}}` to extract three bullet points using a prompt in French.

The output of your prompts can be further manipulated using [Filters](https://help.obsidian.md/web-clipper/filters). Filters are processed after the prompt response is received from the model. For example: `{{"a summary of the page"|blockquote}}` will turn the response into a blockquote.

## Get started

Interpreter works with almost any language model provider, including options that run privately on your device. To set up Interpreter:

## How it works

When Interpreter is enabled *and* your template contains [prompt variables](https://help.obsidian.md/web-clipper/variables#Prompt%20variables), a new Interpreter section is displayed in the extension window, above the **Add to Obsidian** button. This section allows you to select a model and run Interpreter for the current page.

When you click **interpret**, Interpreter sends the page context to your selected model, along with *all* the prompts in your template in one request. Depending on the model provider you choose, this can be an external call or local to your device. The model evaluates your prompts against the page context, and returns its responses. Interpreter then replaces the prompt variables with the response data.

The whole process can take milliseconds or more than 30 seconds depending on the model you use and the amount of data you are processing.

## Context

The term *context* refers to the page data that Interpreter uses to process prompts. The smaller the context, the faster Interpreter runs.

By default, Interpreter uses the entire page HTML as its context, however this can make prompts slower and more expensive than necessary.

You can override the default context in Interpreter **Advanced settings** and define context per [template](https://help.obsidian.md/web-clipper/templates).

To define a more targeted context use [selector variables](https://help.obsidian.md/web-clipper/variables#Selector%20variables) (or other variable types) to interpret a section of the page. For example, you could use the following selector variable in your template's Interpreter context:

```
{{selectorHtml:#main}}
```

This would only run Interpreter on the `#main` element of a web page, if it exists. [HTML processing filters](https://help.obsidian.md/web-clipper/filters#HTML%20processing) like `remove_html`, `strip_tags` and `strip_attr` can be useful to further reduce the context length and speed up processing.

## Models

Privacy

By using a third-party model provider you agree to their terms and privacy policy. Interpreter requests are sent directly to the provider you choose. Obsidian does not gather or store any data about your requests.

### Preset providers

Interpreter includes several preset providers. To use these providers you need an API key which you can get by logging into your provider's account. You will also need to decide which model(s) to use.

| Provider | API key | Models |
| --- | --- | --- |
| Anthropic | [API key](https://console.anthropic.com/settings/keys) | [Models](https://docs.anthropic.com/en/docs/about-claude/models) |
| Azure OpenAI | [API key](https://oai.azure.com/portal/) | [Models](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/models) |
| DeepSeek | [API key](https://platform.deepseek.com/api_keys) | [Models](https://api-docs.deepseek.com/quick_start/pricing) |
| Google Gemini | [API key](https://aistudio.google.com/apikey) | [Models](https://ai.google.dev/gemini-api/docs/models/gemini) |
| Hugging Face | [API key](https://huggingface.co/settings/tokens) | [Models](https://huggingface.co/models?pipeline_tag=text-generation&sort=trending) |
| Meta | [API key](https://llama.developer.meta.com/) | [Models](https://llama.developer.meta.com/docs/models) |
| Ollama | n/a | [Models](https://ollama.com/search) |
| OpenAI | [API key](https://platform.openai.com/api-keys) | [Models](https://platform.openai.com/docs/models) |
| OpenRouter | [API key](https://openrouter.ai/settings/keys) | [Models](https://openrouter.ai/models) |
| Perplexity | [API key](https://www.perplexity.ai/settings/api) | [Models](https://docs.perplexity.ai/guides/model-cards) |
| xAI Grok | [API key](https://console.x.ai/team/default/api-keys) | [Models](https://docs.x.ai/docs/models) |

### Choosing a model

In general we recommend using small models with Web Clipper because they are faster and perform fairly accurately for this task. Examples of smaller models include **Anthropic's Claude Haiku**, **Google Gemini Flash**, **Llama** with 3B or 8B parameters, or **OpenAI's Mini** series of models.

### Custom providers and models

To add a custom provider and/or model go to Web Clipper **Settings** → **Interpreter**:

- **Add provider** to configure preset and custom providers.
- **Add model** to configure preset and custom models.

When adding a custom provider, we recommend that you use their chat completions endpoint for the **Base URL** — it typically ends with `/chat/completions`.

### Local models

#### Ollama

[Ollama](https://ollama.com/) allows you to run language models locally and privately on your device.

Once you have downloaded and installed Ollama, add Ollama using **Add provider** in Interpreter settings. Ollama does not require an API key. Then choose a model from the [model list](https://ollama.com/search). For example if you want to use [Llama 3.2](https://ollama.com/library/llama3.2), click **Add model**, then:

- **Provider:** Ollama
- **Display name:** Llama 3.2, this value is customizable.
- **Model ID:**`llama3.2`, this must exactly match the model ID from Olllama.

**Start the Ollama server**

To allow a browser extension to interact with Ollama you must [give it explicit instruction](https://github.com/ollama/ollama/issues/2308) when running the server, or else you will see a `403` error.

Close the Ollama app, and run the following command in your terminal. The protocol should be changed to your browser's extension protocol if you don't use Chrome or Firefox.

```
OLLAMA_ORIGINS=moz-extension://*,chrome-extension://*,safari-web-extension://* ollama serve
```

Then run your model with Ollama the normal way, e.g.

```
ollama run llama3.2
```