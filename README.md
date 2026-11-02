# profile-readme-ci

I built this as part of my GitHub Developer Program portfolio. It is a reusable GitHub Actions workflow that verifies a profile README on a schedule. A profile page makes claims: links to projects, counts of advisories and writeups, titles and dates. This workflow checks that every link still resolves, that every printed count still matches the record it came from, and that no claim has gone stale while nobody was watching the page.

Status: scaffold. The workflow interface is defined and the verification engine is the next build step.

## What it will do

- Fetch every link in the profile README and report the ones that fail
- Recompute the counts the README prints and compare them against the page
- Flag claims whose source has changed since the page was written
- Report the results as a scheduled run, green when the page is honest and red when it is not

Built by Gavin Blacklock (Epsilon0xCell).
