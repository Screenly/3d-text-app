[![Version](https://img.shields.io/github/v/release/Screenly/3d-text-app)](https://github.com/Screenly/3d-text-app/releases/latest)

# 3D Text Screensaver Edge App

A nostalgic homage to the classic Windows 98 '3D Text' screensaver. This Edge App creates a smooth, bouncing 3D text effect that moves across your screen, complete with metallic gradients and dynamic lighting effects.

## Configuration

The app supports the following settings:

- `text` - The text to display in 3D. If not provided, the screen name will be used.
- `text_color` - The color of the text in hex format (e.g. #9C5FE4). Defaults to brand primary color.
- `background_color` - The background color of the text. If not provided, the default is black.

## Releasing

Pushes to `main` deploy to stage automatically. To release to production, tag a commit on `main` and push the tag (the workflow refuses tags not on `main`):

```bash
git checkout main && git pull
git tag v26.10.0
git push origin v26.10.0
```

Then publish a GitHub Release whose notes list the pull requests merged since the previous release. Add `--draft` to review the notes before publishing:

```bash
gh release create v26.10.0 --verify-tag --generate-notes --title v26.10.0
```
