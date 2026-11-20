# alumni-account-access

A Claude skill for getting back into your university account after graduation and lining up the records grad school applications need.

It has Claude:

- explain what alumni keep (usually just the school email) and what shuts off, and when
- diagnose a failed sign-in: password, MFA (Duo or Google 2-step), or an account closed after inactivity
- draft a help desk request and a registrar request for you to review and send
- point you to official transcripts, degree verification and diploma services
- help you keep the alumni email alive once you're back in

It never sends anything, types your password or SSN digits, or puts your personal details into outside services.

## Install

Copy this folder to `~/.claude/skills/alumni-account-access/`. Copy `templates/profile.example.md` to `profile.md` and fill it in. `profile.md` is git-ignored.

## School references

- `references/new-school.md`: The New School and Parsons. Alumni service cutoffs, alumni email sign-in, password reset, IT Central contacts, transcripts and verification.

For another school, Claude researches its IT and registrar pages and writes a new reference in the same shape.
