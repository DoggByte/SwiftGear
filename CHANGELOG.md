# Changelog

What changed in **SwiftGear**, version by version, from the point of view of someone who uses it.

## [Unreleased]

## [1.5.1] - 2026-11-07

### Added

- **SwiftGear is on GitHub.** Each new version is published as a release with a ready-to-install zip and its checksum, and this is the page the **Check for updates** button in Settings looks at.

### Changed

- **The User Guide's install steps** now explain how to download the zip from GitHub, unzip it into a folder that stays put, load it in the browser and update it later.

## [1.5.0] - 2026-11-07

### Added

- **The User Guide explains the basics.** Every tool's entry now starts with a short **What is ...?** summary of the thing it works with (What is a UUID?, What is a JWT?, What is a subnet?...). It shows only in the User Guide; the How to use box on the tool page is unchanged.
- **Hide the How to use box.** A new **Tool page** option in Settings, **Show the How to use, examples box on each tool**, turns that box off on every tool page. It is on by default, and the help button in the tool header still opens the same text in the User Guide.

### Changed

- **Closing a tool stops what it was doing in the background.** Leaving Bcrypt, RSA key pair generator, Math evaluator, Regex tester or Text diff now frees what they were using, and the clocks and key listeners of Date-time converter, OTP, Keycode info and Device information stop at once. Before, every visit to Text diff or Bcrypt kept using memory until the panel was closed.
- **The regex tester runs one match at a time.** Typing a slow pattern used to start a new run for every keystroke, each lasting up to 2 seconds; a newer run now replaces the older one.
- **Tighter privacy settings.** The extension no longer allows playing recorded video (left over from the removed Camera recorder), and the Check for updates request no longer says which page it came from.

## [1.4.2] - 2026-11-07

### Changed

- **Emoji picker: bold labels.** The Code point, HTML and JS labels on each card are bold, so they stand out from the values.

## [1.4.1] - 2026-11-07

### Changed

- **Emoji picker: one code per line.** The Code point, HTML and JS buttons on each card are now stacked, one per line, instead of flowing side by side.

## [1.4.0] - 2026-11-07

### Added

- **Every tool explains itself.** All 85 tools now have a guide entry with what the tool does, a **Use it for** list of real situations, an **Example** with a real input and its real output, and the controls. The same text shows on the tool's page in a collapsed **How to use, examples** box under the intro, so you do not have to leave the tool to learn it.
- **The emoji picker says what its numbers are.** Each card has three labelled copy buttons: **Code point** (`U+1F680`, now with every code point of a multi-part emoji such as a heart or a family), **HTML** (`&#x1F680;`) and **JS** (the `🚀` escape), and the guide says where to paste each one. Searching by `U+1F680` works as well as `0x1f680`.

### Fixed

- **The emoji list fits the panel.** It was a fixed 600 pixels wide, so it ran off the right edge of a narrow panel (and pushed the search box with it). It now takes the width of the panel and the codes wrap onto the next line.

## [1.3.1] - 2026-11-06

### Added

- **A link to the tool in the User Guide.** Each tool's entry, and a tool's own help page, has a link icon right of its title that opens the tool itself.

### Fixed

- **The version number on the home screen** rests on the same line as the name SwiftGear instead of floating above it.

## [1.3.0] - 2026-11-06

### Added

- **Settings.** A gear button right of the User Guide button opens a Settings page. It can show or hide the descriptions under the tools and the icons left of the tools (both shown by default, changes apply at once in every open panel), shows the installed version and the newest version available, and has an About section with the author, contact address and website. **Check for updates** asks GitHub for the newest release when you press it, in one request that sends nothing about you. It is the only network request the extension can make, and it is never made on its own.
- **A branded home screen.** The header shows the SwiftGear icon, the name and the installed version above the search box. It stays in place while the list scrolls.

### Changed

- **The User Guide gives the contents list 30% of the height and the text 70%,** and every page shares the same spacing around its content.

### Removed

- **The pop-out button, the tab view and the Camera recorder.** SwiftGear is now a side panel only, and no longer asks for the camera. There are now 85 tools.

## [1.2.0] - 2026-11-06

### Added

- **A full User Guide, inside the extension.** Click the book button beside the search box to open it. It has a contents list, a title bar with a search box (highlighting, next and previous match, and an "Only matching sections" option) that stays put while the contents and the text scroll on their own, and an entry for every tool with its options, defaults and tips, plus chapters on installing, finding tools, favourites, the side panel, the right-click menu, remembered settings, keyboard shortcuts, privacy and permissions and troubleshooting. Every tool's header now has a help button that opens that tool's own page in the User Guide, and Back always returns to where the guide was opened from.

## [1.1.1] - 2026-11-06

### Fixed

- **Tool descriptions wrap.** In the tool lists a long description now flows onto the next line instead of ending in an ellipsis, and the tool icon sits at the top of the row, level with the title.

## [1.1.0] - 2026-11-06

### Added

- **Every tool has its own icon,** in the tool lists (home, search results, favorites) and on the tool page. The icons come from the Tabler Icons set.

### Fixed

- **A stray "null".** The Chronometer showed the word null between Start and Reset while stopped; a tool header and the camera picker had the same bug.

## [1.0.0] - 2026-11-06

### Added

- **2 new Data tools.** Phone parser and formatter (country, calling code, valid or not, type, and the international, national, E.164 and RFC3966 formats; the default country follows your browser language) and IBAN validator and parser (valid or the reasons it is not, QR-IBAN, country code, BBAN, friendly format, with valid examples).
- **7 new Text tools.** Lorem ipsum generator, Text statistics (characters, words, lines and bytes; an emoji counts as one character), Emoji picker (about 1900 emojis in groups, fuzzy search by name, keyword, code point or the emoji itself, one click to copy), String obfuscator, Text diff (a side-by-side editor where both sides are editable, light and dark), Numeronym generator (internationalization is i18n) and ASCII art text drawer (over 300 fonts, font and width remembered).
- **10 new Development tools.** Git cheatsheet and Regex cheatsheet, Random port generator, Crontab generator (checks a cron expression and says what it means in plain English), JSON to CSV, SQL prettify and format (20 dialects), Docker run to docker-compose converter (with a docker-compose.yml download), XML formatter, YAML prettify and validator, and Email normalizer. Right-click on selected text now also offers Format SQL, Explain cron expression, Format XML and Prettify YAML.
- **New Images and videos tools.** WiFi QR code generator (open, WPA/WPA2, WEP and WPA2-EAP networks, hidden SSID, colors, PNG download) and SVG placeholder generator (size, colors, font size, custom text; copy the markup or download the SVG).
- **11 new Web tools.** Device information, Basic auth generator, Meta tag generator (Open Graph and Twitter tags), OTP code generator and validator (TOTP and HOTP with a QR code), MIME types, Keycode info, Slugify string, HTML WYSIWYG editor, User agent parser, JSON diff and Outlook SafeLink decoder.
- **12 new Converter tools.** Roman numeral converter, Text to NATO alphabet, Text to ASCII binary, Text to Unicode, YAML to TOML, JSON to TOML, TOML to JSON, TOML to YAML, List converter, XML to JSON, JSON to XML, and Markdown to HTML (with a preview and Print as PDF).
- **6 new Crypto tools.** Bcrypt (hash a string and compare a string with a hash, without ever freezing the panel), Encrypt / decrypt text (AES, TripleDES, Rabbit, RC4), BIP39 passphrase generator (ten languages), RSA key pair generator (256 to 16384 bits), Password strength analyser and PDF signature checker (certificates, signer details, and whether the document changed after signing).

### Changed

- **Math and Measurement tools do much more.** The Math evaluator understands units (5 cm to inch), matrices, complex numbers, your own functions (f(x) = x^2) and statistics, with full-precision results, and stops an expression that never ends after 3 seconds. The Percentage, ETA and Temperature tools start filled in and give exact answers, the Chronometer's Reset zeroes a running timer, and the Benchmark builder can copy a markdown table or a bullet list and remembers everything.
- **Network tools do much more.** The IPv4 subnet calculator reads shorthand and hex forms and shows every address of the block; the range expander shows old and new values side by side; the MAC address lookup shows the whole IEEE record with a Copy vendor info button; the MAC address generator remembers your choices.
- **Development tools and the QR code generator do much more.** The JSON formatter accepts JSON5 (comments, trailing commas, single quotes), sorts keys, highlights the result and remembers your settings. The Regex tester adds flags, shows where each group starts and ends, makes a sample text that matches and draws a diagram of the pattern. The QR code generator has colors with opacity, four error resistance levels, and PNG and SVG downloads.
- **Web, Converter and Crypto tools do much more.** Separate encode and decode cards, examples to start from, more hash and HMAC algorithms, UUID versions 3 and 5, a richer JWT and URL parser, an editable color converter with a picker, bases 2 to 64 in the integer converter, and remembered settings throughout.
- **Tools are listed in a new order:** Crypto, Converter, Web, Images and videos, Development, Network, Math, Measurement, Text, Data.

## [0.2.0] - 2026-11-06

### Added

- **12 new tools, 35 in total.** Network: IPv4 address converter, IPv4 subnet calculator, IPv4 range expander, MAC address lookup (IEEE vendor names built in, works offline), MAC address generator, IPv6 ULA generator. Math: math evaluator, percentage calculator, ETA calculator. Measurement: temperature converter (eight scales), chronometer (laps, keeps running while you use another tool), benchmark builder (means, variance, who is faster).

## [0.1.0] - 2026-11-05

### Added

- **First version:** a side panel (toolbar button or Alt+Shift+D) with search, favorites and right-click on selected text. Works fully offline.
- **23 tools:** token, hash, HMAC, UUID and ULID generators; date-time, integer base, Base64 text, Base64 file, color, case, JSON to YAML and YAML to JSON converters; URL encoder, URL parser, HTML entities, JWT parser and HTTP status codes; JSON formatter and minifier, regex tester, chmod calculator; QR code generator.
- Large JSON numbers keep every digit when formatted, and a regular expression that never finishes is stopped after two seconds instead of freezing the panel.
