# Publishing NOVA on GitHub

This document is for someone publishing the **generic** NOVA template, not their personal study vault.

## Suggested repository details

- **Repository name:** `NOVA-Academic-Workspace` (or any valid repository name you prefer)
- **Description:** A customizable Obsidian vault for students to organize courses, lecture notes, schedules, tasks, exams, and research literature — all in one workspace.
- **Topics:** `obsidian`, `obsidian-vault`, `student-productivity`, `academic-workflow`, `knowledge-management`, `zotero`, `study-planner`
- **Visibility:** Public, when you are ready to share the template.
- **License:** MIT (already included in [`LICENSE`](../LICENSE)). Review the terms and replace the copyright notice if you prefer your legal name or another credit.

## Recommended: create the GitHub README directly

1. Create a **new public repository** on GitHub named `NOVA-Academic-Workspace` (or your preferred spelling).
2. On GitHub's **Create a new repository** screen, choose **Add README: On**, **No .gitignore**, **No license**. Our upload package already provides `.gitignore` and `LICENSE`, but intentionally **does not include `README.md`**.
3. After creating the repository, edit the auto-generated GitHub `README.md` and paste the short public project introduction. Include this relative link to the detailed documentation: `[Read the Complete User Guide](docs/USER_GUIDE.md)`.
4. Extract the NOVA *GitHub upload package*. In GitHub choose **Add file → Upload files**, and upload **the contents of the extracted `NOVA_Academic_Workspace` folder**, rather than the ZIP or enclosing folder. The README you created online stays untouched; the upload contains `START HERE.md`, numbered study folders, `docs/USER_GUIDE.md`, `LICENSE`, and `.gitignore`.
5. **Do not forget `.obsidian/`.** This is a hidden dot-folder containing the vault settings and CSS snippets. On Windows, turn on **View → Show → Hidden items** if required. A local Git client (GitHub Desktop) is a reliable alternative for uploading hidden files and folders.
6. Commit the files. The full guide should now open when you click the **Read the Complete User Guide** link in the GitHub README.
7. In the repository's **Settings**, enable **Template repository** and confirm that **Use this template** appears on the project page.
8. Add the project description and topics under GitHub's **About** section. Download the published repository as ZIP and test opening it as an Obsidian vault.

> **Why there is no README in the upload ZIP:** The public-facing GitHub README is created and maintained **inside GitHub**. Uploading a second README would overwrite it or create a conflicting version. Keep `docs/USER_GUIDE.md` in the uploaded file tree; do not rename it to `README.md`.

## Option: upload using Git on your computer

This is an **alternative**, not an extra step. To publish with Git after creating the repository with a README on GitHub, clone the existing repository first, then copy the extracted NOVA upload-package files (including hidden `.obsidian`) into the clone, keeping its existing `README.md`. Replace `YOUR-USERNAME` with your actual GitHub username.

```bash
git clone https://github.com/YOUR-USERNAME/NOVA-Academic-Workspace.git
cd NOVA-Academic-Workspace
# Copy the extracted NOVA upload-package contents into this folder first.
git add .
git commit -m "Add NOVA Obsidian template and full user guide"
git push
```

Git must be installed and configured for your account. Run the copy step in your file manager before `git add .`; do not run the placeholder comment as a file-copy command. GitHub authentication may require a browser login, credential helper, SSH key or personal access token; never paste access tokens into repository files.

## Before publishing: safety checklist

- Confirm this is the **generic NOVA template**, not `NOVA_Academic_Workspace_Personal` or a customized live vault.
- Check that `01 Courses/` contains only `Course Catalog.md` and no real course folders.
- Check that `04 Library/Zotero Papers/` and `04 Library/Reading Notes/` contain no user papers, highlights or notes.
- Check `08 Attachments/`, `09 Planning/Reviews/`, `.obsidian/` and the entire Git history for private documents, profile data, API keys and local filesystem paths.
- Do not publish books, paid lecture slides, research PDFs or copyrighted images without permission.
- Keep Obsidian plugins installed locally; do not commit plugin executables or cache files.
- Review the MIT license before publication. **Public visibility is not itself a license.**
- Consider adding a real screenshot later, with fictional course names only.

## Keeping the published template clean

Use the public repository as the *source template*. Create a **separate private vault/repository** for your real studies. `gitignore` excludes some machine-specific Obsidian files, but it **does not automatically protect personal notes** — review every commit before pushing.

The following folders have `.gitkeep` placeholder files so GitHub retains their otherwise empty structure. `.gitkeep` files are harmless and can be left in place.

## Documentation

- [README](../README.md) — public project overview
- [Full user guide](USER_GUIDE.md) — complete Obsidian installation and study workflow
- [Setup checklist](../SETUP%20CHECKLIST.md) — first-run checklist
- [Contributing](../CONTRIBUTING.md) — guidelines for pull requests
- [MIT License](../LICENSE) — redistribution conditions
