# CollegeSearch data

Data files for the CollegeSearch desktop app, which downloads them when it starts so its
scholarship and college information stays current.

| File | What it is |
| --- | --- |
| `manifest.json` | Version numbers the app compares with what it already has, plus the dates shown in the app |
| `scholarships.json` | National scholarships: amounts, eligibility, deadlines and links, checked against sponsors' sites |
| `aid.json` | Federal aid programs, each state's aid agency, and places to search further |
| `colleges.tsv` | Figures for about 3,900 U.S. colleges, from the U.S. Department of Education's College Scorecard |

To publish a change, edit the file and raise the matching number in `manifest.json`
(`scholarships` covers `scholarships.json` and `aid.json`; `colleges` covers `colleges.tsv`).
The app ignores any file that does not read cleanly.

Scholarship deadlines change every year. Entries with `"confirmed": false` carry dates from
directories or a previous cycle; always confirm on the sponsor's own site.
