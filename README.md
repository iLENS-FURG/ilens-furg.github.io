# iLENS Website

Hugo website for the iLENS research area.

The website is intentionally data-driven. Do not manually edit generated person/project/publication pages; edit `iLENS-FURG/ilens-data` instead.

## Local preview

Install Hugo Extended, then:

```bash
hugo server -D
```

To preview current sample data:

```bash
python ../ilens-automation/scripts/generate_content.py .
hugo server
```

## GitHub Pages

The workflow in `.github/workflows/pages.yml` builds the site whenever the website changes or when `ilens-data` dispatches `data-updated`.

For private source repositories, use separate least-privilege secrets in the website repository:

- `ILENS_DATA_TOKEN`: fine-grained token with **Contents: read** on `iLENS-FURG/ilens-data`.
- `ILENS_AUTOMATION_TOKEN`: fine-grained token with **Contents: read** on `iLENS-FURG/ilens-automation`.

The website workflow never stores source data or automation credentials in the repository.
