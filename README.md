# Nostr Explain

A single-page educational website that provides a comprehensive introduction to **Nostr** (Notes and Other Stuff Transmitted by Relays) — the censorship-resistant, decentralized communication protocol.

## What This Is

This is a static HTML page designed as a long-form guide (~20 min read) covering the Nostr protocol from the ground up. It is styled as a clean, documentation-like site with a fixed sidebar for navigation and syntax-highlighted code examples.

## Topics Covered

- **What is Nostr?** — Overview of the protocol, its origins (created by fiatjaf in 2020), and its core philosophy of radical simplicity.
- **Why Nostr Matters** — Comparison with centralized social media: identity ownership, censorship resistance, data portability, and fault tolerance.
- **Core Concepts** — The three building blocks: **Keys** (secp256k1 keypairs for identity), **Events** (signed JSON objects as the unit of data), and **Relays** (WebSocket servers that store and forward events).
- **How Nostr Works** — The client-relay communication protocol using `EVENT`, `REQ`, and `CLOSE` messages over WebSockets.
- **Keys & Identity** — Key management, bech32 encoding (npub/nsec), and browser extensions (nos2x, Alby) for secure signing.
- **Relays In Depth** — Relay validation, policies, access control, NIP-11 relay info documents, types of relays (public, paid, community, outbox, search), running your own relay, the outbox model (NIP-65), and relay synchronization.
- **Code Examples** — Practical JavaScript and Python snippets using `nostr-tools` and `pynostr`:
  1. Generating a keypair
  2. Creating and publishing an event
  3. Connecting to multiple relays with `SimplePool`
  4. Subscribing to events with filters
  5. Publishing a NIP-65 relay list
  6. Running a relay with `nostr-rs-relay`
- **NIPs (Nostr Implementation Possibilities)** — Overview of key NIPs including NIP-01 (basic protocol), NIP-02 (follow lists), NIP-04/44 (encrypted DMs), NIP-05 (DNS verification), NIP-19 (bech32 encoding), NIP-23 (long-form content), and NIP-57 (zaps).
- **Use Cases** — Social media, Bitcoin Lightning zaps, long-form publishing, and decentralized identity.
- **Ecosystem** — Popular clients (Damus, Amethyst, Snort, Primal), developer libraries, and browser extensions.

## Tech Stack

- Pure HTML + CSS (no build step, no dependencies)
- CSS custom properties for theming
- Responsive layout with a collapsible sidebar
- Scroll-based active section highlighting via `IntersectionObserver`

## Usage

Open `index.html` in any web browser — no server required.

```sh
# Or serve locally
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## License

This project is open source.
