# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A collection of single-file browser games. Each game is a fully self-contained `.html` file with no build step, no dependencies, and no frameworks — pure HTML, CSS, and JS in one file.

## Running Games

Open any `.html` file directly in a browser:
```
start tictactoe.html
start rockpaperscissors.html
```
Or via cmd: `cmd /c start "" "<full path to file>"`

## Architecture

Each game file follows the same structure:
1. `<style>` — all CSS inline in `<head>`
2. `<body>` — semantic HTML layout
3. `<script>` — all game logic inline at the bottom

**Shared visual style across all games:**
- Background: `#1a1a2e`, card surfaces: `#16213e`, accent/buttons: `#e94560`
- Font: `'Segoe UI', sans-serif`
- Hover transitions: `transform: scale(1.04–1.07)` + background shift to `#0f3460`
- Score board: three `.score-box` divs (player / draw / opponent) with `.label` + `.value`
- Status line: fixed-height `#status` element, color-coded by outcome
- Player color: `#a0c4ff` (blue), Computer/Opponent color: `#ff6b6b` (red), Draw: `#aaa`

Any new game added to this repo must follow this same visual convention.

## Git & GitHub

- Remote: `https://github.com/sewalkorkmaz/browser-games`
- Branch: `master`
- Commit style: short imperative subject line, optional body for context

**Commit and push frequently throughout all work.** After every meaningful change — adding a feature, fixing a bug, updating a file — stage, commit, and push immediately. Never leave completed work uncommitted. This ensures no progress is ever lost and the GitHub history always reflects the current state of the project.

Each logical unit of work should be its own commit. Do not batch unrelated changes into one commit.
