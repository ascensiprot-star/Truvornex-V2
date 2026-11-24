# Localization and Accessibility

Language, country, currency, tax jurisdiction, time zone, and legal territory are distinct. Support locale-specific dates, numbers, currencies, addresses, pluralization, long text, and right-to-left layout where relevant. All strings must be localizable; canonical machine values stay separate from translated labels. Machine translations must be labeled and original content retained when needed.

Do not hardcode claims such as support for 195 countries, 186 languages, or any arbitrary theme count unless generated from maintained, tested configuration. Country support is expressed as capability flags with source and review date.

Use platform semantics, screen-reader labels, logical focus order, scalable text, sufficient contrast, reduced motion, accessible touch targets, keyboard/switch support where relevant, captions/transcripts, and clearly identified errors. Never communicate status by color alone.

Test on Android and iOS with assistive technology, representative locales, long translations, RTL, currency/date formats, and fallback behavior. Accessibility is a release criterion.
