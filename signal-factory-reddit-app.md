---
layout: default
permalink: /signal-factory-reddit-app/
title: SignalFactory Reddit App
---

# SignalFactory Reddit App

SignalFactory is a personal, local research and content-intelligence tool used by the site owner to follow public technical discussions about AI, machine learning, developer tools, and software infrastructure.

This page documents the intended Reddit API use for the SignalFactory app.

## App purpose

The app is designed to read public Reddit posts and selected public comment metadata from AI-related communities at a low polling frequency.

Planned communities include:

- r/LocalLLaMA
- r/MachineLearning
- r/ChatGPT

The purpose is to identify high-signal public discussion themes, developer objections, technical pain points, product updates, and useful public links for private research and editorial planning.

## Data collected

SignalFactory only needs a limited set of public metadata and short excerpts needed for local analysis:

- source URL
- post or comment title where available
- subreddit name
- public timestamp
- author-visible public metadata when returned by the official API
- short public excerpts for ranking and deduplication
- outbound links shared in public posts

The app does not collect private messages, private user data, moderator-only content, or non-public Reddit data.

## What the app does not do

SignalFactory does not:

- post to Reddit
- vote on Reddit
- send messages
- moderate communities
- automate user-facing Reddit behavior
- scrape Reddit pages outside the official API
- redistribute raw Reddit datasets
- sell Reddit data
- train, fine-tune, or sell machine-learning models using Reddit data

## Storage and retention

The app stores limited public metadata locally for the owner's private research workflow.

If Reddit content is deleted, removed, or no longer available through the official API, SignalFactory should treat it as unavailable and avoid using it as an active source in future outputs.

## API and rate-limit behavior

SignalFactory is intended to use Reddit's official API with a unique user agent, OAuth credentials, low polling frequency, and API rate-limit handling.

The app should read and respect Reddit API rate-limit headers and should not attempt to bypass Reddit's access controls.

## Contact

For questions about this app or its data use, use the site contact page:

[Contact NingClaw Software Workflow Lab](/contact/)
