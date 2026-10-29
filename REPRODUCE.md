# How this repository was made (Tonga)

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Tongan Legislation, Attorney General's Office (Current Revised Edition, legislation history tables) | <https://www.ago.gov.to/cms/legislation/current-revised-edition/by-title.html> | 2026-10-28 | private use; commercial reuse needs permission (site meta "rights") |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | Constitution of Tonga | 17 | 1988-12-31 to 2020-12-04 |
| `criminal-offences` | Criminal Offences Act | 18 | 1988-12-31 to 2020-12-04 |

The build made 35 commits:

| Commits | Kind |
| ---: | --- |
| 2 | first version of an act |
| 29 | one law on its in-force day |
| 4 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 100 laws in the record.
- 64 tags.

## Dates

Each commit is dated at noon (Pacific/Tongatapu) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Interpretation Act (Cap. 1.02), s. 3(1): "An Act to which His Majesty's Assent has been given shall come into operation on the day of publication in the Gazette, unless the contrary intention appears"; proviso: Acts pursuant to clause 79 of the Constitution come into operation on the day signed by His Majesty. https://www.ago.gov.to/cms/images/LEGISLATION/PRINCIPAL/1903/1903-0006/InterpretationAct_3.pdf

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `d39003419b19eb935210fa61e48c38e5839618664ab0003822e4b6e165c80501` (467984 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3e59cb6f05eccb94a9ec14431a7f6781221e83ef`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- English text is built. The AGO also publishes each Revised Edition in Tongan; by the Interpretation Act (Cap. 1.02) s. 21 the Tongan version of a law takes precedence, so the English text is the official English version, not the controlling one.
- Each act starts at the 1988 Revised Edition, the oldest text the AGO publishes (first_law null): the 1875 Constitution as granted and the earlier Acts are not online in an official text. The 1988 edition is dated 31 December 1988, the day it states it was revised to; the 2016 and 2020 editions take the 'Date Commenced' of the AGO legislation history table (31 December 2016; 4 December 2020).
- Provision wording is compared word for word between editions after normalising quotes, dashes and spaces; where only the layout differs, the earlier text is kept so no false change appears.
- History notes are not law text: the 1988 edition's inline italic notes ("(Amended by Act 3 of 1976.)") and the endnote markers of 2016/2020 are removed from the text and used only to date and credit changes.
- Part headings are kept in one 'parts' file per act; the long title, enacting words and the edition's revision statement are left out.
- The Constitution's 2016 Revised Edition is not listed in the AGO history table but is still published at ConstitutionofTonga.pdf_2.pdf (also captured by the Internet Archive on 2020-11-04); it is used as version 2.
- Constitution, clause 37: the 1988 Revised Edition prints it as amended by Act 13 of 1966 (in force 1990-07-01), so before then it reads as a placeholder and the printed words arrive on 1990-07-01.
- Constitution, clause 50: the 1988 Revised Edition prints it as amended by Act 13 of 1966, Act 12 of 1990 (in force 1990-07-01, 1990-08-08), so before then it reads as a placeholder and the printed words arrive on 1990-08-08.
- Constitution, clause 84: the 1988 Revised Edition prints it as amended by Act 13 of 1966 (in force 1990-07-01), so before then it reads as a placeholder and the printed words arrive on 1990-07-01.
- Constitution, clause 85: the 1988 Revised Edition prints it as amended by Act 13 of 1966 (in force 1990-07-01), so before then it is absent (inserted by that Act) and the printed words arrive on 1990-07-01.
- Constitution, clause 87: the 1988 Revised Edition prints it as amended by Act 13 of 1966 (in force 1990-07-01), so before then it is absent (inserted by that Act) and the printed words arrive on 1990-07-01.
- Constitution, clause 90: the 1988 Revised Edition prints it as amended by Act 12 of 1990 (in force 1990-08-08), so before then it reads as a placeholder and the printed words arrive on 1990-08-08.
- Constitution, clause 91: the 1988 Revised Edition prints it as amended by Act 13 of 1966, Act 12 of 1990 (in force 1990-07-01, 1990-08-08), so before then it reads as a placeholder and the printed words arrive on 1990-08-08.
- Constitution, clause 92: the 1988 Revised Edition prints it as amended by Act 13 of 1966, Act 12 of 1990 (in force 1990-07-01, 1990-08-08), so before then it is absent (inserted by that Act) and the printed words arrive on 1990-08-08.
- Constitution, clause 95: the 1988 Revised Edition prints it as amended by Act 13 of 1966 (in force 1990-07-01), so before then it is absent (inserted by that Act) and the printed words arrive on 1990-07-01.
- Constitution, clause 7: changed by Act 23 of 1990, Act 17 of 2003 between the 1988 Revised Edition (Cap. 2) and the 2016 Revised Edition (Cap. 01.01); the source gives no text between them, so it reads as a placeholder from 1990-07-18 and the 2016 Revised Edition (Cap. 01.01) words arrive on 2003-11-21.
- Constitution, clause 31A: changed by Act 39 of 2010, Act 20 of 2010, Act 1 of 2011 between the 1988 Revised Edition (Cap. 2) and the 2016 Revised Edition (Cap. 01.01); the source gives no text between them, so it reads as a placeholder from 2010-09-24 and the 2016 Revised Edition (Cap. 01.01) words arrive on 2011-03-16.
- Constitution, clause 70: changed by Act 18 of 1999, Act 20 of 2010 between the 1988 Revised Edition (Cap. 2) and the 2016 Revised Edition (Cap. 01.01); the source gives no text between them, so it reads as a placeholder from 1999-11-03 and the 2016 Revised Edition (Cap. 01.01) words arrive on 2010-11-24.
- Constitution, clause 83B: changed by Act 39 of 2010, Act 1 of 2011 between the 1988 Revised Edition (Cap. 2) and the 2016 Revised Edition (Cap. 01.01); the source gives no text between them, so it reads as a placeholder from 2010-09-24 and the 2016 Revised Edition (Cap. 01.01) words arrive on 2011-03-16.
- Constitution, clause 83C: changed by Act 39 of 2010, Act 1 of 2011 between the 1988 Revised Edition (Cap. 2) and the 2016 Revised Edition (Cap. 01.01); the source gives no text between them, so it reads as a placeholder from 2010-09-24 and the 2016 Revised Edition (Cap. 01.01) words arrive on 2011-03-16.
- Constitution, clause 85: changed by Act 39 of 2010, Act 20 of 2010 between the 1988 Revised Edition (Cap. 2) and the 2016 Revised Edition (Cap. 01.01); the source gives no text between them, so it reads as a placeholder from 2010-09-24 and the 2016 Revised Edition (Cap. 01.01) words arrive on 2010-11-24.
- Constitution, clause 86: changed by Act 39 of 2010, Act 20 of 2010 between the 1988 Revised Edition (Cap. 2) and the 2016 Revised Edition (Cap. 01.01); the source gives no text between them, so it reads as a placeholder from 2010-09-24 and the 2016 Revised Edition (Cap. 01.01) words arrive on 2010-11-24.
- Constitution, clause 88: changed by Act 39 of 2010, Act 20 of 2010 between the 1988 Revised Edition (Cap. 2) and the 2016 Revised Edition (Cap. 01.01); the source gives no text between them, so it reads as a placeholder from 2010-09-24 and the 2016 Revised Edition (Cap. 01.01) words arrive on 2010-11-24.
- Criminal Offences Act, section 24: changed by Act 25 of 1990, Act 17 of 1999, Act 4 of 2000 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1990-12-19 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2000-08-04.
- Criminal Offences Act, section 25A: changed by Act 25 of 1990, Act 19 of 2012 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1990-12-19 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2012-12-27.
- Criminal Offences Act, section 48: changed by Act 17 of 1999, Act 5 of 2006 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1999-11-03 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2007-01-03.
- Criminal Offences Act, section 56: changed by Act 25 of 1990, Act 19 of 2012 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1990-12-19 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2012-12-27.
- Criminal Offences Act, section 57: changed by Act 25 of 1990, Act 19 of 2012 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1990-12-19 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2012-12-27.
- Criminal Offences Act, section 83: changed by Act 25 of 1990, Act 19 of 2012 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1990-12-19 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2012-12-27.
- Criminal Offences Act, section 112: changed by Act 12 of 1995, Act 19 of 2012 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1995-10-10 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2012-12-27.
- Criminal Offences Act, section 115: changed by Act 17 of 2001, Act 19 of 2012 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 2001-09-13 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2012-12-27.
- Criminal Offences Act, section 118: changed by Act 17 of 1999, Act 17 of 2001 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1999-11-03 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2001-09-13.
- Criminal Offences Act, section 188: changed by Act 12 of 1995, Act 16 of 2004, Act 19 of 2012 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1995-10-10 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2012-12-27.
- Criminal Offences Act, section 197: changed by Act 8 of 1991, Act 18 of 2005 between the 1988 Revised Edition (Cap. 18) and the 2016 Revised Edition (Cap. 10.09); the source gives no text between them, so it reads as a placeholder from 1991-08-15 and the 2016 Revised Edition (Cap. 10.09) words arrive on 2006-01-10.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code with Claude Opus 5.5 (claude-opus-5-5) wrote Lexifina's code and chose the sources and editions; it did not write or alter any legal text. Lexifina's code is deterministic and runs no model; every line of law comes from an official PDF as retrieved.
