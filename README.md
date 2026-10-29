# Stillblade

A mobile-first Three.js sword duel: ivory samurai versus an AI ronin, first to three rounds. No build step or server backend.

## Play locally

Run `node serve.cjs`, then open `http://localhost:4173`. For a phone on the same Wi-Fi, use your computer's LAN IP and port 4173 (your firewall must allow access). ES modules require HTTP; opening index.html directly is not supported.

Run `node combat.test.cjs` for combat behavior checks.

Mobile: drag the left stick to move, tap Strike, and hold Guard. The first 190 ms of a guard can parry an incoming hit, staggering the attacker. Desktop: WASD, Space, Shift; Escape pauses. Each hit deals 25 damage. Strikes and blocks cost stamina; stamina regenerates when you lower your guard. Fighters automatically face each other. An attack's windup leaves a deliberate opening.

## GitHub Pages

1. Create a GitHub repository and upload these files, including `.github/workflows/pages.yml`, to its `main` branch.
2. In the repository's **Settings → Pages → Build and deployment**, choose **GitHub Actions**.
3. Run **Deploy to GitHub Pages** in the Actions tab, or push a commit to `main`.
4. The deployment supplies your Pages URL, typically `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

All asset paths are relative, so repository subpaths work. The workflow uploads the static folder directly. Three.js is pinned to 0.170.0 on jsDelivr; fonts come from Google Fonts with local fallback fonts. Internet access is required for Three.js.

This is single-player 1v1 against AI. It does not include network multiplayer, accounts, or a backend. Audio is synthesized locally and off by default. The application pauses when the tab loses focus.
