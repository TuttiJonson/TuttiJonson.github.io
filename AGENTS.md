# AGENTS.md

This file provides guidance to Claude Code and other AI coding agents when working with code in this repository.

Plain HTML, CSS, and JavaScript only. Never add a framework or a library —
no React/Vue/etc., no jQuery, no CSS framework (Tailwind, Bootstrap), no
bundler, no package manager, no `node_modules`, no CDN `<script>`/`<link>`
includes (including web fonts). Every page loads only its own markup,
`css/styles.css`, and `js/main.js`. Use only what the browser's DOM/CSS/JS
gives you natively.
