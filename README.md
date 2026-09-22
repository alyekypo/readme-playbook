# readme-playbook

How to write a README that a stranger trusts enough to keep reading. In 2026 the reader's default assumption is that your page was generated; everything below is about disproving that in the seconds before they close the tab.

## How READMEs are actually read

Skim order: the project name, the first sentence, the install command. Judgment happens in seconds, above the fold; the rest of the page confirms a judgment already made.

- Nobody reads top to bottom. They scroll hunting for the one section that answers their question, and leave if it cannot be found in one sweep.
- Every element that carries no information — decoration, marketing, boilerplate — costs the elements next to it their credibility.
- The reader owes you nothing. A README is answered questions, not a pitch.

## The credibility problem

Generated READMEs flooded the platform, and readers pattern-match against them. The tells: emoji in section headings, a badge wall under the title, a "Features" list of bolded lead-ins, a "Why X?" section arguing with itself, a diagram that restates the paragraph above it, a table of contents on a page that fits one screen, a footer thanking the reader for their attention.

None of these is a crime alone. Together they read as a page nobody wrote wrapped around code nobody reviewed, and the reaction is not conscious: the tab closes. The fix is not to imitate the style more carefully. It is a page where every line answers a question a stranger actually has.

## The header

Three elements: the project name as the only H1, one sentence saying what it is and who it is for, and nothing that is not information.

- The first sentence carries the page: what it is, who it is for, what it replaces. No taglines, no adjectives, no "simple, powerful, and flexible".
- Badges: one line at most, each answering a question (license, build status, version), and only the kind that reads repository state. A static badge asserting a quality — "clean code", "awesome" — is an assertion wearing a claim's clothes. If you cannot name what would turn a badge red, delete it; one lying badge makes every other claim on the page suspect.
- No logo walls, banner images, or artwork dividers. No emoji in headings, ever.

## The body, in the order the reader needs it

1. **Install.** The exact command, prerequisites, supported versions.
2. **Quick start.** The smallest input that produces visible output. Copy-pasteable, and verified by running it exactly as written on a clean checkout.
3. **Usage.** The three to five tasks most people do. A sixth means the rest move to `docs/`.
4. **Limits and non-goals.** What it does not do, and the known ceiling. The most trust per line of any section.
5. **License.** One line and a link.

Skip a section rather than write a placeholder: an empty "Roadmap" with "coming soon" announces an unfinished page. Keep nothing for completeness: a section exists because a stranger asks the question, not because a template has the slot.

## Claims must be verifiable

Every number and status on the page names the thing that produced it, or comes down.

- Performance: the number, the workload, the environment, the revision — or no number. "Blazing fast" is a negative claim: it announces that the page exaggerates.
- Compatibility: versions you test in CI now, not versions you once tried.
- A command the reader can rerun beats a sentence they must believe. Put the command next to any number you typed by hand.

## Diagrams

One test: the reader must hold three or more things in their head at once, and the relationship between them is not linear. Anything else is a numbered list or a sentence.

- Never one per section, never a restatement of the paragraph above, never decorative.
- Text source in the repository (Mermaid or ASCII in a fence) so the diagram can be reviewed in a diff; every edge labeled; about seven nodes at most.
- Verify on the rendered page, not through a markdown API: the API renders a Mermaid fence as a code block, the repository page renders the diagram.

## Tables

A table earns its place when items share two or more attributes and comparison is the point; anything smaller is a list. Fill every cell, put units in the header, keep it to two to five columns. A blank cell is an unanswered question.

## Length

A README is a front page, not a manual. When it outgrows a few screens, material a reader *consults* moves to `docs/`, material a reader *executes* stays, and each moved section leaves one link behind. Deleting beats moving: a page that documents a dropped feature is worse than a short page. The previous version of this file was 346 lines, including a table of measured badge pixel widths; it is gone, not moved.

## Checklist before publishing

- Read the first screen as a stranger: the name, the sentence, the install command. Is it enough to know what this is and whether to continue?
- Every claim names its source; every number names its measurement.
- Every badge reads repository state and answers a question.
- The quick start was run, copy-paste, exactly as written, on a clean checkout.
- No emoji headings, no marketing sections, no table of contents on a one-screen page.
- The rendered page was checked once: external images are proxied by the host, and a dead badge shows as a broken image, not an error.

## License

[MIT](LICENSE)
