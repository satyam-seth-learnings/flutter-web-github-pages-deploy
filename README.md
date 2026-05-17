# flutter_web_github_pages_deploy

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Learn Flutter](https://docs.flutter.dev/get-started/learn-flutter)
- [Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Flutter learning resources](https://docs.flutter.dev/reference/learning-resources)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.



# GitHub Pages Deployment 

## Key Points in This Workflow
1. Push to `main` triggers the workflow.
2. Workflow checks out the repo and builds Flutter web.
3. Switches to `deploy` branch (creates if not exists).
4. Copies the web build into `docs/`.
5. Commits and pushes changes back to deploy branch.

## How It Works
1. Build outputs into a temporary folder (`web-build`).
2. Switches to `deploy` branch.
    - Creates it if it doesn’t exist.
3. Syncs `web-build` to `docs/` (this is what GitHub Pages serves from main/docs if you configure Pages, or from root of `deploy` branch if you point Pages there).
4. Commits only the updated files.
5. Pushes to `deploy` branch.

## GitHub Pages Setup Options
- Option 1: Serve from `docs/` on `deploy` branch
    - Go to repo → Settings → Pages → Source → `deploy branch / docs folder`.
- Option 2: Serve from root of `deploy` branch
    - Set Pages source → `deploy branch / root`