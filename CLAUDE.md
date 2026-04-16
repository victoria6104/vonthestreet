# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A single-page personal website for Victoria Araujo. No build tools, frameworks, or dependencies — just a single `index.html` file served statically.

## Architecture

Everything lives in `index.html`: HTML structure, CSS styles (in a `<style>` block), and JavaScript (in a `<script>` block at the bottom).

**Navigation model:** A sticky nav bar at the top controls which screen is visible. Screens are `<section>` elements with `id="home"`, `id="menu"`, and `id="about"`. The `showScreen(id, btn)` JS function toggles the `.active` class to swap screens — no routing library, no page reloads.

**Screens:**
- `#home` — profile photo (`your-photo.jpg`) and name card
- `#menu` — grid of cards (Portfolio, Resume, Contact)
- `#about` — bio text

## Development

Open `index.html` directly in a browser — no server required. For live reload during editing, use VS Code's Live Server extension or any static file server:

```bash
npx serve .
```
