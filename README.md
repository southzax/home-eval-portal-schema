# home-eval-portal-schema
Python script that converts a Caspio app export into a database diagram, applied to a home-accessibility evaluation portal I designed.

Why:

I designed this Caspio app for a physical therapist starting a home-accessibility evaluation business. The goal was to help people with limited mobility adapt their homes instead of moving to a care facility. Evaluators could record home details, photos, and notes to support their recommendations, then return for a follow-up visit to confirm the changes were made.

He originally asked for a quick Google Form. After considering where the business was headed, I recommended a low-code app instead, for:

Security: better protection for patient information. Role-based access: individual logins, so as the team grew, each evaluator would see only their assigned patients. Records that evolve: forms can be edited after submission, and reports run on demand. Follow-up visits: a follow-up evaluation generated from the original, to confirm recommendations were implemented.

Additional security features: I designed three login types (admins, evaluators, and patients), each limited to the data it needed. Logins ran through "active" views, so access could be revoked without deleting historical records. Patient usernames were randomly generated IDs, which gave stable keys for reports, better protected patient identities, and made logins harder to guess. Passwords used Caspio's secure password type, and sessions timed out after two hours.

The client was happy with the result but closed the business for personal reasons before using the app in production. This repo preserves the design.
