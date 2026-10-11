---
name: zenith-publish
description: Submit a public GitHub app commit to Zenith and follow its review with the CLI.
---

# Zenith publish

Complete one-time browser sign-in, GitHub connection, and terms on the developer's account. An authorized agent can then prepare and submit from the CLI. Ensure the GitHub repository and selected commit are public, and pin a full commit SHA that exists on GitHub. Commit the final deployable Compose file, Dockerfile or image workflow, and app source. Supply a real screenshot of the running app, not a placeholder or synthetic image.

Run `zenith publish --commit <full-sha> --metadata listing.json --screenshot path.png` from the repository. The metadata file supplies listing fields, and screenshots may be repeated. Read any warning that the submitted commit differs from the last tested version. The warning is useful context, not a submission gate. Keep the returned receipt. Use `zenith publish status` for review status and feedback. `zenith publish resubmit` retries a rejected submission, `zenith publish update-code` submits a different commit, and `zenith publish update-listing` changes only listing data while retaining the last pinned commit. These commands accept the same relevant metadata and screenshot flags.

A submission enters review. It is not a live catalogue listing until approved and published.
