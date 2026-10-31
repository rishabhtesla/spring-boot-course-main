# Frontend Utilities

Utilities are small reusable functions that are not tied to one screen. Examples here include shared constants and helpers for formatting or shortening text.

Find where a utility is imported before changing it, because a shared helper can affect many pages. Keep these functions focused and predictable; presentation formatting belongs here only when multiple components can reuse it.

**Practice:** find a price-formatting helper and one caller. Try a harmless formatting change and check every place that uses it.
