# 054 — Examen

A nightly Ignatian Examen for the AppADay project. Walks through the five traditional movements of the Examen, gratitude, light, review, sorrow, and grace, one screen at a time, with a flickering candle and a slow breathing ring to set the pace.

**Live:** https://augustineiacopelli.github.io/appaday-054-daily-examen/

## What it does

Each of the five movements opens with its own guiding question and a short prompt drawn from the traditional structure of the Examen. A breathing ring syncs to a four-second in-out cycle so the pace of reflection isn't rushed, and an optional journal field lets the person write a line or two without ever requiring it.

The Grace movement replaces a plain prompt with a tappable grid of the seven Catholic virtues, the four cardinal virtues and three theological virtues. Tapping any virtue opens a modal with a short catechetical description before the person names which grace they're asking for in their own words.

The Sorrow movement includes an optional AI reflection. If an Anthropic API key has been added in Settings, the person's private journal entry for that movement alone can be sent to Claude, which gently suggests two to five possible areas for examination of conscience, organized by which of the Ten Commandments they relate to. The reference list behind this reflection is drawn from a full ten-commandment examination of conscience, so the categories Claude prefers to name match traditional Catholic confession preparation rather than generic suggestions. A disclaimer makes clear this is a private aid to prayer, not a confession, and that only a priest absolves.

A five-dot progress trail tracks movement through the sequence, and the closing screen ends on the Glory Be with a quiet count of how many nights have been kept on that device.

## Why it's built this way

The Examen is meant to be a five-minute nightly habit, not a heavyweight tool, so it stays deliberately lighter than a dedicated confession-preparation app would be. The AI reflection is opt-in and scoped to a single movement's entry, never the full night's journal, to keep the feature proportionate to a nightly habit rather than turning every evening into a full examination of conscience.

## Stack

Single-file vanilla HTML, CSS, and JavaScript. No build tools, no frameworks. The AI reflection calls the Anthropic API directly from the browser using the person's own API key, stored only in that browser's local storage and never committed to the repo.

## Category

Spirituality (S)
