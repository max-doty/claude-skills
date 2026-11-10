# Pinned plugins

The marketplace on this branch (`.claude-plugin/marketplace.json`) lists four plugins.
Each one copies skills from [oaustegard/claude-skills](https://github.com/oaustegard/claude-skills),
as they stood at commit `e44f32e` (2026-11-10), when they were read before
installing. The rest of the branch is upstream's tree at that commit. `main`
follows upstream and is not installed from.

| plugin | skills |
|---|---|
| `declauding` | declauding, without upstream's Stop hook |
| `review` | challenging, verifying-claims |
| `code` | tree-sitting, assessing-impact, declaring-invariants |
| `checks` | gating, reasoning-semiformally |

Install:

    claude plugin marketplace add <owner>/claude-skills --sparse .claude-plugin pinned
    claude plugin install declauding@claude-skills-pinned

To update: sync `main` with upstream, read what changed in these skills, copy
them into `pinned/` again, and bump the versions.
