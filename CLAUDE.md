# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a React 19 demo application called "Stargazers" - a character showcase app that displays cast members with modal details. It serves as exercise files for the LinkedIn Learning course "Claude Code 4: Agentic Coding for Professional Developers".

## Commands

- `npm run dev` - Start Vite development server
- `npm run build` - Build to `docs/` directory
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

## Architecture

**Tech Stack:** React 19, Vite, Pico CSS, React Compiler (beta)

**Build Configuration:** Vite outputs to `docs/` with relative base paths (`./`) for GitHub Pages deployment.

**Data Flow:**
- `App.jsx` manages global state (cast list, selected member)
- Cast data loaded from `public/cast.json` via fetch
- Member selection passed down via `onChoice` callback props
- Modal state controlled by `memberInfo` in App

**Key Components:**
- `App.jsx` - Root component, fetches cast data, manages modal state
- `Nav.jsx` - Navigation with cast dropdown and theme toggle
- `ListCast.jsx` - Grid display of cast member thumbnails
- `Modals.jsx` - Member detail dialog with navigation arrows
- `ToggleTheme.jsx` - Dark/light theme switcher using Pico CSS

**Static Assets:** Images and cast.json in `public/`, served at root path.
