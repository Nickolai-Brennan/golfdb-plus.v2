# GolfDB+ Event PDF Index

Open the official publisher links to research tournament setup, agronomy, field composition, tee times, and daily hole locations.

| File | Contents |
| --- | --- |
| [2026 event and GCSAA source index](2026-event-source-index.csv) | GolfDB+ event IDs and schedule dates, exact PGA TOUR Media event URLs, verified GCSAA fact sheet links, and coverage gaps. Multiple source URLs can describe the same tournament. |
| [Sony Open in Hawaii PDF index](2026-sony-open-media-pdf-index.csv) | Event-specific PDF links listed in Tournament Details and Other Information. The manifest records the published link and round where shown. |

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
