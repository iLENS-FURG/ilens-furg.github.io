# iLENS Deployment

The public website is built from private `ilens-data` and `ilens-automation` repositories using GitHub Actions. Secrets use least-privilege fine-grained tokens.

Build gates: validation → graph → generation → API → Hugo build → Pages deploy.
