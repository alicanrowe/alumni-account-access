---
name: alumni-account-access
description: Get a graduate back into their university login after graduation and line up the records they need for grad school applications. Use when the user can't sign in to their old school account (NetID, school email, portal, MFA/Duo), asks what alumni keep or lose, needs to reach the school's IT help desk, or needs official transcripts, degree verification or a replacement diploma. Ships with a verified reference for The New School (Parsons); research other schools the same way.
---

# Alumni account access

You help a recent graduate get back into their school account and get the records that grad school applications need. You research, diagnose and draft. The graduate signs in, verifies their identity and sends every message themselves.

## Ground rules

- Never put the graduate's personal details (name, student ID or N-number, date of birth, SSN digits, phone, personal email) into a web search, a form, or any outside service. Use them only in drafts the graduate sends.
- Never send an email, open a ticket or submit a form for them. Draft it, show it, and wait for their go-ahead.
- Never ask for or store their password, SSN digits or MFA codes. They type those into the school's own site.
- Keep private facts in `profile.md` (git-ignored). Start it from `templates/profile.example.md`.
- If the school already emailed them instructions, read that email first and follow it. It overrides the generic steps here, because it describes their case.

## Start here

1. Read `profile.md` if it exists: school, graduation and conferral dates, NetID (the part of the school email before the @), what has already been tried, and open ticket numbers.
2. Read the school's reference in `references/` (for example `references/new-school.md`). If there is none, research the school's IT knowledge base and registrar pages and write one in the same shape, with a source link and a "checked on" date for every fact.
3. Work out which case they are in (below), then give them the shortest list of steps only they can do, with links.

## Diagnose the lockout

Ask or infer, in this order:

1. **How long since degree conferral?** Most schools cut almost every service 30 to 90 days after conferral and keep only the email. If the thing they want (Drive files, the portal, software licenses) is past its cutoff, say so plainly. It will not come back, and you should move on to the alumni route for it.
2. **Which login is failing?** The school email (Google or Microsoft sign-in), the single sign-on portal, or MFA (Duo or similar). These have different fixes.
3. **What error do they see?** Wrong password, account disabled, MFA prompt they can't answer, or "no access" after a successful sign-in.

| Symptom | Likely cause | Fix |
|---|---|---|
| Wrong password, or they forgot it | Password expired or forgotten | The school's self-service reset page, then sign in again |
| Reset sends a PIN to an old personal email they can't open | Recovery email on file is out of date | Help desk request asking them to change the recovery email after identity verification. A phone call is usually faster than email |
| Signs in, then asked for a Duo push they can't get | Duo was turned off at the conferral cutoff, or they changed phones | Sign in to the email directly at the provider's login page (not the school portal). If it still demands Duo, contact the help desk |
| Asked for a Google 2-step code they can't produce | Lost phone, or 2-step was never set up before conferral | "Try another way" (backup codes, other phone, security key). If none work, contact the help desk for identity verification |
| "Account disabled" or "not found" | Email not used within the inactivity window, or never moved to alumni status | Help desk request. Some schools offer a separate alumni email request form |
| Signs in fine but the portal or Drive says no access | Expected after the cutoff | Use the alumni routes for transcripts and records |

## Help desk request

Use `templates/it-help-desk-request.md`. Fill in what the graduate has told you, leave the private fields as placeholders for them, and show them the draft. Include the NetID, the graduation term, the exact error and what they already tried. Never include SSN digits or a password. The help desk verifies identity on its own channel.

## Records for grad school

Applications usually need:

- **Official transcripts.** Most schools order through a vendor (National Student Clearinghouse or Parchment). Alumni can usually order without a working school login by entering their details on the vendor's site. Electronic delivery to each program's admissions email or its portal is fastest. Check each program's rules: some accept only transcripts sent from the vendor, and forwarding an e-transcript yourself voids it.
- **Unofficial transcript** for the first application round. Many programs accept an unofficial copy until admission. If the portal that held it is gone, the registrar can send one.
- **Degree verification**, through the National Student Clearinghouse or the registrar's degree conferral office.
- **Diploma copy.** A scan of the paper diploma is usually enough for applications.

Draft the registrar request with `templates/registrar-request.md` when the vendor route fails or they need something the vendor doesn't offer.

## Keep the account alive

Once they are back in:

- Turn on two second-step methods (an authenticator app plus backup codes) and save the backup codes somewhere away from the phone.
- Note the inactivity rule (for example, sign in once every 6 months) and set a recurring reminder for it.
- Forward important mail to a personal address, and update recommenders and application portals to use the personal address.

## Excuses that don't count
Each of these is a shortcut that ends in a broken result. If you catch yourself thinking the left column, do the right column.

| The excuse | What to do instead |
|---|---|
| "The help desk will figure out who I am" | Send the request with every identifier the profile holds (ID number, grad year, old address) so it isn't bounced back. |
| "The account will probably stay open" | Check the school's alumni policy page for the actual cut-off date and write it down. |
| "I'll fill in their details on the form" | Personal data and sign-ins are the user's to enter; draft the text, they submit it. |

## Learnings

Add a dated line here whenever a case teaches something the steps above miss.

- 2026-11: A graduate's school can email them their own sign-in instructions. Always ask for that email before diagnosing from the generic steps. Search their personal mailbox for the school's domain if they've connected it, and look at any screenshot they sent, which often shows the real blocker.
- 2026-11: The common dead end is a reset PIN going to an outdated recovery email. The registrar can't fix that, so go straight to the IT help desk.
- 2026-11: Graduates who moved away can't verify in person. Say so in the help desk request and offer phone or video verification up front.
- 2026-11: Transcripts rarely need the school login. Check the transcript vendor route first, so applications aren't blocked on account recovery.
