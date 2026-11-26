# GolfDB+ Event PDF Index

Open the official publisher links to research tournament setup, agronomy, field composition, tee times, and daily hole locations.

| File | Contents |
| --- | --- |
| [2026 event and GCSAA source index](2026-event-source-index.csv) | GolfDB+ event IDs and schedule dates, exact PGA TOUR Media event URLs, verified GCSAA fact sheet links, and coverage gaps. Multiple source URLs can describe the same tournament. |
| [Sony Open in Hawaii PDF index](2026-sony-open-media-pdf-index.csv) | Event-specific PDF links listed in Tournament Details and Other Information. The manifest records the published link and round where shown. |

| [The RSM Classic PDF index](2026-rsm-classic-media-pdf-index.csv) | 40 distinct URLs across 42 listed round and document placements. Two course-specific hole-location files appear in both the round 1 and round 2 cells. |
| [Hero World Challenge PDF index](2026-hero-world-challenge-media-pdf-index.csv) | Three distinct URLs for the field, scorecard, and course map. |

## 2026 coverage

As reviewed on November 26, the season index covers 49 events. GCSAA has 30 verified PDF URLs across 29 events, including two posted Masters copies. The season CSV identifies the 20 remaining gaps under `no_verified_sheet_found`. Its `gcsaa_listed_date` field records the publisher’s sheet label date. The scheduled dates describe the competition, with exceptions and differences documented in `date_note`.

| Event | Competition and venue | Media PDF coverage |
| --- | --- | --- |
| [Sony Open in Hawaii](https://pgatourmedia.pgatourhq.com/tours/2026/pgatour/sonyopeninhawaii) | Jan 15–18 at Waialae Country Club | 29 URLs. Previously indexed. |
| [The RSM Classic](https://pgatourmedia.pgatourhq.com/tours/2026/pgatour/thersmclassic) | Nov 19–22 scheduled at Sea Island Golf Club (Seaside and Plantation). [PGA TOUR reported a Nov 23 finish](https://www.pgatour.com/article/news/daily-wrapup/2026/11/23/round-4-the-rsm-classic-fedexcup-fall-finale-scores-leaderboard-monday-finish-2027-pga-tour-cards-aon-next-10). The [GCSAA sheet](https://gcsaa.org/docs/default-source/tournament-fact-sheets/pga-tour/2026/11-19-the-rsm-classic-%28pga-tour%29.pdf?sfvrsn=9f5fa23e_2) covers both courses. | 40 URLs, including 13 under Tournament Details and 27 under Other Information. |
| [Hero World Challenge](https://pgatourmedia.pgatourhq.com/tours/2026/pgatour/heroworldchallenge) | Dec 3–6 at Albany GC, Bahamas | Three URLs under Other Information. Round PDFs and a GCSAA sheet are pending. |

The date notes also document the difference between the Grant Thornton Invitational’s event week and its [competition schedule](https://grantthorntoninvitational.com/tournament-info/schedule-of-events/).

The media indexes contain 72 distinct PGA TOUR Media PDF URLs across three events. The status `listed_on_official_page` describes link presence on the publisher’s event page. For the RSM and Hero manifests, `section_group` retains the subsection for icon-only links and `venue_scope` records the course when the publisher identifies one. A blank round indicates the page did not assign a round.

## Daily workflow

1. Find the course and tournament date in the GolfDB+ PGA schedule. Cross-check the event ID in the year-events-id tab. For a routine run, check active events, events starting in the next seven days, and events ending in the past seven days. For a targeted run, use the requested course and date.
2. Open the official PGA TOUR Media schedule. Follow the event link as published. The final URL segment varies, even within the same season. Check the tournament name, edition, venue, and scheduled dates on the event page. The media schedule's week-of date may precede the first round.
3. Open Tournament Details and Other Information in the browser. Record every event PDF link, including icon-only controls. Capture the display title, section, round when shown, original filename, and publisher URL. Use the event's source page for provenance.
4. Find the GCSAA document in the season index. Check the relevant organizer's category for majors. If the index has no match, use the event start month/day and slug as a lookup fallback. The publisher varies zero padding, abbreviates some event names, and sometimes has two links for the same event. Record a direct link only after confirming the PDF and edition.
5. Update the GitHub indexes only when source links or coverage change. Report links found, missing sheets, date discrepancies, and any sources that could not be checked. Leave unresolved IDs blank. The public repository carries source links and metadata. Obtain applicable permission before redistributing PDF copies.

## Official sources

- [PGA TOUR Media schedule](https://pgatourmedia.pgatourhq.com/schedule)
- [PGA TOUR Media Sony Open in Hawaii](https://pgatourmedia.pgatourhq.com/tours/2026/pgatour/sonyopeninhawaii)
- [GCSAA tournament fact sheets](https://gcsaa.org/who-we-are/media/tournament-fact-sheets)
- [PGA TOUR Media terms](https://pgatourmedia.pgatourhq.com/static-assets/page/footer/files/terms-of-service.pdf)
- [GCSAA terms](https://www.gcsaa.org/terms-of-use)

## Implementation Notes

- **Assumptions.** Scope follows the GolfDB+ 2026 PGA schedule, including its team and qualifying entries.
- **Risks.** Workbook dates, media week dates, and dates printed on fact sheets may differ. Use independent fields and flag conflicts.
- **Next Steps.** Recheck unresolved GCSAA entries as the publisher adds fact sheets.
- **Alternatives.** Use an organizer's official document index when its event does not have a PGA TOUR Media document page.
- **Performance Considerations.** Reuse verified event links and check new or changed entries first.
- **Maintenance Considerations.** Refresh the season schedule and preserve earlier links when a publisher changes documents.
