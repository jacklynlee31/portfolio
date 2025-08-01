---
title: Hypermode - Modus Quickstart
pubDate: Dec 20 2024
description: "Improving the developer documentation for Modus, an AI modeling tool"
---


## Hypermode - Modus Quickstart

At Hypermode, I worked on improving the developer documentation for Modus, an AI modeling tool that lets users build and deploy language models trained on their own data. Modus is designed to help teams create AI-driven applications without needing to manage or fine-tune the infrastructure themselves.

The audience for these docs was developers looking for a fast, reliable setup experience. These were people who wanted to get started quickly, not spend time troubleshooting or digging through sparse examples.

## Challenges

When I joined, the docs were functional but had some gaps. They hadn't been tested in a while, and there were a few places where the docs seemed to just drop off with no resolution for the user. The Quickstart guide was a perfect place to start learning more about Modus and find my footing as I got ready to test the existing documentation.

## My Process

- Hands-on testing: Before diving into a formal docs audit, I tested Modus myself. I created a Modus agent and tested it in both Go and AssemblyScript.
- Found and reported bugs: I uncovered a few bugs during my testing. There were a few code samples that didn't work, and others that were missing from the docs altogether. I flagged these issues to engineering, and this led to some fixes in both the docs and the codebase.
- Improved the clarity of the docs: I validated each step in the flow, rewriting unclear sections and filling in any gaps. I added key steps that had been missing, including `hyp login` and `modus dev`.
- Added missing end steps: The original docs ended abruptly, so I added final steps that helped users add a model and log in using the CLI to complete the experience.

## Results

By the end of the project, I'd shipped a Quickstart guide that was:
- Validated through hands-on testing.
- Clearer and more structured for task-based learning.
- More helpful for new users getting started with Modus.


### Link

👉 <a href="https://web.archive.org/web/20250415232614/https://docs.hypermode.com/modus/quickstart" target="new">Modus Quickstart</a>