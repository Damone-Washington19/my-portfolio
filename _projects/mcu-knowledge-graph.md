---
title: MCU Knowledge Graph
date: 2026-06-18
layout: project
tags: [python, graphs, ai, data]
tech: [Python, NetworkX, Matplotlib, BeautifulSoup, Wikipedia API, Requests]
repo: https://github.com/Damone-Washington19
---

A multi-phase Python knowledge graph system that maps relationships between Marvel Cinematic Universe characters using real data from the Wikipedia API. The project combines web traversal, API pagination, graph construction, and visualization into one data-driven workflow.

**Phase 1 - Web Crawler:** Built a BFS-based crawler using `requests` and `BeautifulSoup` that starts from a seed URL, extracts cross-domain hyperlinks, and constructs a directed domain-level connection graph. Edge weights track link frequency so repeated connections become visible in the graph.

**Phase 2 - Wikipedia Integration:** Integrated the Wikipedia API to query MCU character categories, retrieve up to 500 characters, and fetch each character's internal article links. The API layer handles paginated responses so the system can work with larger result sets instead of one-off manual data collection.

**Phase 3 - Character Relationship Graph:** Combined the crawler and API workflow into a character network. BFS traversal is constrained to a whitelist of known MCU characters, which keeps the graph focused on meaningful relationships. Nodes are scaled by degree to surface high-influence characters such as Iron Man and Captain America.

**Recruiter takeaway:** This project shows backend utility automation, API integration, graph modeling, and data visualization skills in a single Python system.

Key techniques: directed graph construction, BFS traversal with depth control, REST API consumption, node-degree-scaled graph visualization, pagination handling.
