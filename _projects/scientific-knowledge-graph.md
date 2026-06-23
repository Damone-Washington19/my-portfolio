---
title: Scientific Concept Knowledge Graph
date: 2026-06-01
layout: project
tags: [python, graphs, ai, data]
tech: [Python, NetworkX, Matplotlib, JSON]
repo: https://github.com/Damone-Washington19
---

A knowledge graph visualization tool that transforms structured JSON data into a navigable, labeled graph of semantic relationships between scientific concepts.

Graph nodes represent concepts and edge labels encode the type of relationship between them — for example, "Incubation → *facilitates* → development" or "controlled conditions → *include* → temperature." This models how an AI reasoning system would represent domain knowledge.

The project demonstrates a core technique in AI knowledge representation: converting raw relational data into a graph structure that can be traversed, queried, and reasoned over. Built with `NetworkX` for graph construction and `Matplotlib` for visualization, with a `spring_layout` force-directed algorithm to automatically position nodes for readability.

Key techniques: directed graph construction from JSON, edge attribute labeling, force-directed layout, knowledge representation fundamentals.
