# demo-kubernetes-template

Use this template to bootstrap your Kubernetes-based hands on cloud environment.

Includes a documentation stack (mkdocs) in the `docs` folder.

## Installing docstack

```
pip install -r requirements-docs.txt
```

Start docs:

```
mkdocs serve -a localhost:8000
# or python -m mkdocs serve -a localhost:8000
```

## Enabling Asana Integration

There is a GitHub action which fires whenever a GitHub issue is `opened` and create a new task in Asana for a given workspace and project.

If you don't need / want this, just delete the YAML file.

To set this up, your new repo needs to have 3x GitHub Action Secrets created (settings > secrets and variables > Actions > New repository secret)

- `ASANA_PAT` ([how to generate an Asana PAT](https://developers.asana.com/docs/personal-access-token))
- `ASANA_WORKSPACE` (when you're on the `Home` page it's the ID after `/home/` eg. `2222` in `https://app.asana.com/0/home/2222`)
- `ASANA_PROJECT` (when you're on a project page it's the first URL portion: eg. `1234` in `https://app.asana.com/0/1234/5678`)
