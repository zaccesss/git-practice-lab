# 13: Undoing Mistakes

I use this module to practise picking the right undo command for the situation, then getting work back when I picked the wrong one.

| Part | What it covers |
| --- | --- |
| [13.1: Exercise](13.1-exercise) | Restore, amend, the three kinds of reset and revert, each on purpose |
| [13.2: Extra Practice](13.2-extra-practice) | Reverting a merge, recovering a deleted branch, detached HEAD and safer force pushes |
| [13.3: Self-Test](13.3-self-test) | Questions with no answers shown, to check what actually stuck |

## Why this matters to me

Most Git panic comes from not knowing which undo is safe. The rule I want automatic: anything already pushed and shared gets `git revert`, anything still only on my machine can be rewritten. [Module 09](../09-advanced) uses the reflog once, this module makes recovery a habit.
