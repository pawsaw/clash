# Example Mapping

A structured way to turn a vague story into rules you can build and test against — four kinds
of statement, traditionally four colours of card.

| Card | What it is | In a spec |
|---|---|---|
| Story | The user story under discussion | The `As a... I want... so that...` heading |
| Rule | One testable business constraint | `### Rule: Should/Must ...` |
| Example | A concrete instance that makes a rule unambiguous | `The one where ...` |
| Question | An unknown only the user can resolve | Asked live, then deleted from the saved spec |

A healthy map has a handful of rules, one or two examples each, and few or no questions left by
the end. A story with many open questions still standing isn't ready to build.

## Rules

- One rule, one constraint. Split anything joined by "and".
- State every rule as "Should..." or "Must...".
- Rules describe business behavior, not implementation — no endpoints, screens, or class names.

## Examples

- Default to "The one where..." with real numbers: *The one where a host sets a cap of 5 and
  the 6th person to join is waitlisted.*
- Cover the normal case first. Add more examples only for a boundary or a genuinely different
  outcome.
- Don't add two examples that differ only in a number or a name when the outcome is the same.

## Counter-examples

- A counter-example is a valid boundary or exclusion the rule deliberately doesn't cover — never
  a bug report.
- Give at least one per rule where a meaningful edge case exists: zero, a missing value, exactly
  at a limit.

## Questions

- Raise one whenever the rule depends on a decision only the business can make.
- Resolve each with `AskUserQuestion`, one at a time, offering a few sensible options.
- Fold the answer into the rule, then delete the question. The saved spec has none left.
