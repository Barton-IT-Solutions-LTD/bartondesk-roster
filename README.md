# bartondesk-roster

The independent mirror of the BartonDesk staff list, served by GitHub Pages at
<https://barton-it-solutions-ltd.github.io/bartondesk-roster/roster.json>.

`roster.json` is signed with the Barton IT Solutions organisation key and lists only
anonymous device fingerprints, so it is safe to publish: anyone can read it, but nobody
can change it without the signature failing. BartonDesk customer apps fetch it alongside
the copy on the relay and use the newest valid one, so a compromised relay can't hide a
revoked technician by serving an old list.

Don't edit `roster.json` by hand. It is committed automatically by
`BartonDesk-Console owner publish` on the owner's PC.

Keep this repo **separate from the relay's infrastructure**, and protect the GitHub
organisation with 2FA: an attacker would need to compromise both the relay and this repo
to replay an old list, and even then any list expires within 7 days.
