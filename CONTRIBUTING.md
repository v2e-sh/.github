# Contributing to v2e-sh

These are homelab infrastructure repositories. This guide applies org-wide;
individual repos may add a `CONTRIBUTING.md` with repo-specific notes.

## Workflow

1. Branch from `main` (`feat/...`, `fix/...`, or `chore/...`).
2. Make your change and keep commits small and focused.
3. Open a pull request against `main`. CI must pass before merge.
4. Prefer squash-merge to keep history readable.

## Before you push

Run the checks the repo's CI runs, locally:

- **v2e-tf** — `tofu fmt -recursive` and `tofu validate`
- **v2e-ansible** — `ansible-playbook --syntax-check` (and `ansible-lint` if available)
- **v2e-compose** — `docker compose -f <stack>/compose.yml config -q`
- **v2e-templates** — `shellcheck` the build scripts

## Secrets

Never commit real secrets. Commit `*.example` templates instead:

- Terraform: `terraform.tfvars.example`, never `*.tfvars` or state files.
- Compose: `.env.example` and `secrets.sops.yaml.example`.
- Ansible: use Vault; never commit vault passwords.

## Style

Match the existing style of the file you're editing. Keep changes minimal and
avoid unrelated reformatting in the same PR.
