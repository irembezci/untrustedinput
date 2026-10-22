---
title: Prompt Injection
date: 2026-10-22 10:00:00 +0300
language: en
category: Prompt Security
type: Explainer
author: untrustedinput
description: What Prompt Injection is, how it appears, and how to approach it in security research.
tags: [AI Security, LLM, Direct Prompt Injection, Indirect Prompt Injection]
---

Prompt Injection is a family of attacks that attempt to influence instructions a model is expected to follow. The content may come directly from a user or be embedded in a document, web page, or tool output the model processes.

The concept helps us understand not only how a model responds to a particular request, but also how an application distinguishes instructions, data, and content from external sources.

## The core idea

An AI application often processes system instructions, user input, and content from external sources together. These sources have different levels of trust. Prompt Injection examines whether the model or application handles those boundaries as intended.

A meaningful test looks beyond whether the model produces a particular string. It also considers whether the application protects sensitive data, respects permissions, and limits tool use appropriately.

## Common forms

### Direct Prompt Injection

Conflicting or manipulative content is supplied to the model directly through the user's message.

### Indirect Prompt Injection

The content appears in a source the model reads later, rather than in the user's message. Examples include a document, web page, search result, or tool output.

## Responsible evaluation

Test only systems you are explicitly authorized to assess, and stay within the defined scope. Decide what would count as impact in advance: for example, access to sensitive information, an unauthorized action, or a measurable policy failure.

Document the test conditions, impact, and reproducible steps. Protect real user data and systems outside the authorized scope.

## Related topics

- [Evasion](/evasion/evading-safety-checks/)
- Instruction Hierarchy
- Retrieval-Augmented Generation (RAG)
