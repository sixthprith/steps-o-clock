# Baddie Baddie Steps'o Clock

Private analytics page for a group step challenge (Sept 8 - Dec 5, 2026), served from GitHub Pages.

The page ships no readable data. Names, step counts and the written analysis live in an AES-256-GCM blob inside index.html; the key is derived from the passphrase with PBKDF2-SHA256 (250,000 iterations) in the browser. Without the passphrase the file is ciphertext.

GitHub Pages is a static host with no server-side authentication, so the gate is real encryption rather than a JavaScript check. Anyone holding the passphrase has the data permanently.
