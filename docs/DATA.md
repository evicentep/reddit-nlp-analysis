# Supplied data inventory

Counts were calculated directly from the attached JSON files; no Reddit API calls were made.

| Community | Filtered threads | Filtered comments | Train comments | Test comments |
| --- | ---: | ---: | ---: | ---: |
| Autism | 40 | 875 | 625 | 275 |
| Chemistry | 40 | 875 | 621 | 274 |
| Cooking | 40 | 1,000 | 700 | 300 |
| Investing | 40 | 875 | 625 | 275 |
| Python | 40 | 875 | 571 | 275 |
| Soccer | 40 | 850 | 550 | 273 |
| **Total** | **240** | **5,350** | **3,692** | **1,672** |

The separate OpinionesPolemicas corpus contains 10 threads and 500 comments. Its moderation-results JSON has 500 records, each with `comment_id`, `text`, `zsl`, `fsl` and `cot` fields.

The six `*_resumido_FINAL.json` files are derived artifacts containing generated summaries. Their presence is evidence of saved results, not proof of factual quality. `split_summary.txt` records a 70/30 split by threads with seed 42; this does not imply exactly 70/30 of comments because threads contain different numbers of comments.

Filtered records contain post/comment text, usernames, timestamps, Reddit IDs and URLs. They are not anonymised. This documentation package excludes bulk JSON files and includes aggregate statistics instead. The original files remain in the supplied private archive. The MIT licence applies to original code/documentation, not to Reddit users' writing or external datasets.
