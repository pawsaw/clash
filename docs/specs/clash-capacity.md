# Clash Capacity

**As a host, I want to cap how many people can join my clash, so that the venue doesn't get
overcrowded.**

## Rules

### Rule: Must accept a join while accepted participants are below capacity

- The one where capacity is 5 and 3 people are already accepted — the next join is accepted.

### Rule: Must waitlist a join once capacity is reached

- The one where capacity is 5 and 5 people are already accepted — the next join is waitlisted,
  not rejected.
- Counter-example: The one where capacity is 5 and exactly 4 people are accepted — the 5th join
  is still accepted, not waitlisted. The line is "at capacity", not "one below it".

### Rule: Must accept every join when no capacity is set

- The one where capacity is not set and 50 people have already joined — the next join is still
  accepted.

## Resolved decisions

- **Lowering capacity after people have joined:** does not retroactively waitlist anyone
  already accepted. It only affects joins from that point on.
