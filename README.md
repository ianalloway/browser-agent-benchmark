# Browser Agent Benchmark

Most agent demos skip the part that breaks in production: real websites.

This repo is a public companion to Ian Alloway's post, **The browser is the real agent benchmark**, and captures a practical checklist for evaluating browser-capable AI agents.

- Substack: https://allowayai.substack.com/p/the-browser-is-the-real-agent-benchmark
- Hugging Face Space: https://huggingface.co/spaces/ianalloway/browser-agent-benchmark
- Static HF demo: https://ianalloway-browser-agent-benchmark.static.hf.space

## Core idea

An AI agent that cannot reliably operate a modern authenticated browser is not ready for much of the real internet.

The hard part is not calling an API. The hard part is handling:

- persistent authenticated browser profiles;
- MFA/CAPTCHA/human handoff without leaking credentials;
- iframe switching;
- Shadow DOM traversal;
- ProseMirror, Quill, and other rich-text editors;
- passkey/WebAuthn prompts that sit outside the DOM;
- responsive layout shifts;
- final-state verification with receipts.

## The bar

If an agent claims it posted, submitted, updated, or paid for something, it should produce a receipt:

- final URL;
- DOM state;
- server response;
- public page check;
- screenshot;
- durable artifact ID.

**Receipts over vibes.**

## Use this checklist

See [`checklist.md`](./checklist.md) for a compact, scored evaluation rubric with production-ready gates and critical-failure conditions.
