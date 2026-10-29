# Tonga: law history in git

The law of Tonga as a git history: one file per provision, one commit per edition on the day it took effect. `git blame` names the edition behind every clause; `git log` lists every change to a clause; picking a date gives the text in force that day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `to/`.

**What is in it now**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `constitution/` | Constitution of Tonga | 17 | From the 1988 Revised Edition (31 December 1988) to the 2020 Revised Edition (4 December 2020) |
| `criminal-offences/` | Criminal Offences Act | 18 | The same editions, with the amending Acts between them |

## Dates

- Each commit is dated at noon, Pacific/Tongatapu, on the day the version took effect, as given by the Attorney General's Office legislation history table ("Date Commenced"). Default commencement is Interpretation Act s. 3(1): the day of Gazette publication.
- The English text is built; the Tongan text prevails in a conflict (Interpretation Act s. 21).

## Limits

- **Acts since the 2020 Revised Edition are not replayed.** The newest version is the 2020 Revised Edition. Later amendments (for example Constitution Acts of 2018, 2021 and 2025, and Criminal Offences amendments of 2022 and 2025) are not yet in the record.
- Where several Acts changed a clause between two editions, the clause changes once, between the first and last of them; the commit notes say so.
- Text comes from the PDF text layer. One extraction defect in the 2020 Constitution (clause 19 prints "s hall") was treated as no change. The newest version was compared word by word against the 2020 Revised Edition PDF; every body word is present.
- Only the two acts above are built.

## Source and licence

Official texts from the Attorney General's Office (https://www.ago.gov.to). Official legislative texts are excluded from copyright by the Copyright Act, s. 5(b); see `LICENSE`. Lexifina's arrangement is CC0.
