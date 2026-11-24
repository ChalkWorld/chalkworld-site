---
layout: post
title: First entry and a little philosophy
date: 2026-11-24
description: The gap Chalk World is built around. The frame it uses to fill it.
pinned: true
---

This blog is a running log of the Chalk World build. What follows is the ongoing journey of the work. This is the first real entry.

The premise starts with a gap. LLMs are good at producing text about a drawing, and even competent at producing the drawing or rendering by means of code. They are not, by default, good at spatial reasoning at large, or at keeping a drawing's spatial facts true over multiple turns. Place a few objects in a frame, come back a few turns later and ask about the distance or relation between them, and the model will answer confidently but often wrongly as the session drifts. Nothing structural holds those placements between prompts. The LLM is redrawing (coding) it each time, from scratch, out of held context.

Chalk World's thesis is a frame around that gap. LLMs are optimized to reason about language. Code is language. Geometry can be code. In CW the canvas is a verifiable source of truth that lets both the user and the LLM see and point to things and agree on them. The LLM doesn't hold the canvas code in context; it's prompted to understand what the canvas is, how it behaves, and what it's allowed to draw. With that in place, the LLM is freed to reason about spatial relationships and think critically against a shared source of truth, the canvas itself. The structure around all of it, what the geometry means, how the canvas is set up, how module domain logic is applied, how the human and the model talk through it, is prompting through carefully crafted documents. Documents, all the way down.

While the canvas is integral to using CW, it is also disposable. It serves as a means to visually render the truth-state objects the user can see. How those objects and their metadata are encoded and saved externally is what provides continuity between sessions. That could be pure geometry, plants on a landscape, game pieces on a board, or notes on a staff.

I have built Chalk World primarily using Claude. Claude was chosen because it's been the consistent best fit as an LLM platform to act as project manager across sessions, from project tooling in the early days to GitHub integration and long-running coordination work today. Gemini and ChatGPT have shown up at various points along the way too (testing, pressure-breaking early versions, philosophy conversations that shaped the frame above). But the sustained work has been with Claude. The method and protocols that have evolved to actually get this built (the way sessions hand off, the way documents carry the project's reasoning across time) are their own story, and arguably as instrumental to CW existing in its current form as the engineering itself. A later post gets into that. I do not have any formal code training, and the code that is needed is minimal. Chalk World is about finding the balance of constraining an LLM in the right ways to set it free.

The project has already seen its first major refactor, and that work is still ongoing. After the first versions of CW showed the concepts all worked, it became clear that scaling the project required building it differently. CW has gone from living in a single web-based chat session driving a canvas to incorporating Supabase, Railway, Chainlit, and LangGraph. This decouples the architecture, allows CW to be LLM-agnostic, and builds out a base framework for the domain modules to run on top of as the project scales.