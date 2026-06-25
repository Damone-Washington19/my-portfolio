---
title: MCU Knowledge Graph
date: 2026-06-18
layout: project
tags: [python, graphs, ai, data]
tech: [Python, NetworkX, Matplotlib, BeautifulSoup, Wikipedia API, Requests]
repo: https://github.com/Damone-Washington19
---

A multi-phase knowledge graph system built in Python that maps relationships between Marvel Cinematic Universe characters using real data from the Wikipedia API.

**Phase 1 - Web Crawler:** Built a BFS-based web crawler using `requests` and `BeautifulSoup` that traverses websites starting from a seed URL, extracts cross-domain hyperlinks, and constructs a directed domain-level connection graph. Edge weights track link frequency between domains.

**Phase 2 - Wikipedia Integration:** Integrated the Wikipedia API to programmatically query the MCU character category, retrieve up to 500 characters, and fetch each character's internal article links - all using paginated API requests to handle large result sets.

**Phase 3 - Character Relationship Graph:** Combined both systems to build a full MCU character network. BFS traversal is constrained to a whitelist of known MCU characters, ensuring only meaningful connections are drawn. Nodes are scaled by degree (connection count) to highlight high-influence characters like Iron Man and Captain America.

Key techniques: directed graph construction, BFS traversal with depth control, REST API consumption, node-degree-scaled graph visualization, pagination handling.
