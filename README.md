# github-intake

The whole contents of the public intake repo, `JoeClacks/Crunchify`: its issue forms and nothing
else. That repo holds issues and `.github/` only, never code (`docs/ticket-workflow.md`
§ "Public GitHub vs. private Forgejo"), so this directory is its source and the public repo is a copy.

**Publishing a change here is by hand**, because no box carries a GitHub credential. From a clone of
the public repo, copy `.github/` across, commit and push to its default branch.

**The site's links depend on the field ids.** `$lib/report-link` fills a form by query parameter
named after a field's `id`, so renaming an `id` or a form's filename breaks the prefill silently on
GitHub's side. `src/lib/report-link.test.ts` reads these files and fails first.
