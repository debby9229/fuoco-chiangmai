⚠️ TOKEN BUDGET: This project uses shared Claude.ai quota. Keep all operations minimal — no explanations, no summaries, just execute commands. Batch all file edits into single operations. Never read files unless strictly necessary.

# FUOCO — Chiang Mai Field Guide

## What this project is
A premium digital food guide for Chiang Mai sold at €20. Single HTML file (index.html). Anti-tourist editorial voice. Dark UI, fire/amber palette. Deployed on Netlify via GitHub.

## My role
Creator, editor, developer (with Claude Code). I'm not a developer — I give objectives, Claude Code executes.

## Editorial voice
Opinionated, specific, never generic. Reads like a friend who actually lives there, not a travel blog. No filler adjectives. Honest takes included for every listing.

## Tech stack
- Single file: index.html (currently ~70KB)
- Map: Leaflet.js
- Fonts: Syne, Instrument Serif, DM Sans
- Colors: dark background, fire/amber accents
- Filters: by category (Street Food, Sit Down, Coffee, Wine, Bakery) + time (Lunch, Dinner, All Day)
- Hosting: Netlify (auto-deploy from GitHub)
- Repo: fuoco-chiangmai on local Mac + GitHub

## Current status
15 listings live:
- Street Food (8): Chef Apple, Neng's Clay Oven Roasted Pork, Kaprao Nueanuea, Khao Soi Khun Yai, Kaoneaw Mamuang, Ba Mee Man, Kam-Paeng Sausage, Cherng Doi Roast Chicken
- Sit Down (7): Talung Southern Thai, Tong Tem Toh, Maadae Slow Fish Kitchen, Khao-Sō-i, Chawee, Magnolia Café, Blackitch
- Target: 40-50 listings before launch
- No per-place photos yet (gradient placeholders)

## How to work on this project
- Always work inside ~/fuoco-chiangmai/ folder
- The actual code lives there, not in this CLAUDE folder
- This file is context only
- After each session update memory.md with what changed

## Photo update workflow
When user runs `python3 convert-webp.py listing-N-*.png && ./ship.sh "..."`, immediately after shipping also update index.html slides for that listing and ship again — no confirmation needed. Never read index.html before the edit; grep for the exact `coverImg:"", slides:[]` line and edit directly. Slides always follow pattern: cover + sequential numbered files (2 through N).

## Rules
- Never break the single-file structure
- Keep file size under 150KB
- Always git commit after meaningful changes
- Test filters work after any structural change
