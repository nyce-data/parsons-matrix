# The Parsons Matrix

**Live site: [https://sdiggs.github.io/parsons-matrix/](https://sdiggs.github.io/parsons-matrix/)**

The Parsons Matrix maps who works where in research data stewardship. It places each initiative on three axes: the data disciplines it covers, the stakeholders it serves, and the functions it performs. The axes come from the landscape pilot form. Initiatives that have answered the form are plotted from their own responses; the rest are estimates that get replaced as responses come in.

## What's on the page

- A rotatable 3D cube with a show/hide button for each initiative.
- A switch between all placements and self-reported placements only.
- A "color by" switch between initiative and funder type (federal, philanthropy, host institution, volunteers and small grants, unfunded).
- A placement table marking each initiative as self-reported or estimated.
- What the first responses show, and questions about the form itself.

Filled dots are self-reported answers. Hollow rings are estimates.

## The axes

- **Data disciplines (8):** Federal, Energy, Extreme Weather & Hazards, Environmental Health & Justice, Geospatial & Remote Sensing, Health & Medicine, Physical Sciences, Socioeconomic.
- **Stakeholders (7):** Data Producers, Data Resilience Community, Data Users, Decision Makers, Community Organizers, Media & General Public, Funders.
- **Functions (13):** Data Collection, Data Standards & Quality, Data Preservation & Stewardship, Data Management & Repositories, Data Integration & Interoperability, Data Access & Usability, Innovation & Tool Development, Data Prioritization & Strategic Planning, Community Engagement & Application, Stakeholder Engagement & Partnerships, Data Network Coordination, Advocacy, Policy, & Legal, Funding & Business Models.

The functions run along the data lifecycle, from collection through use, followed by the work that supports the whole chain.

## Status

As of November 8, 2026, two of eleven initiatives have answered the pilot form: NYCE's Climate Data Stewardship Initiative and Public Environmental Data Partners (PEDP). The other nine (KCF's PVSI, the Data Foundation's CCED, CRRDI, the AGU Data Resilience Project, the Data Rescue Project, CODAN, NIH GREI, EDGI, and OEDP) are estimates by Steve Diggs. Funding entries are also his estimates, since the form doesn't ask about funding.

## Adding a response

All placements live in one JavaScript array (`O`) near the bottom of `index.html`. To add a pilot response, find the initiative's entry, copy its answers into `d` (disciplines), `s` (stakeholders), and `f` (functions) using the exact axis labels, set `src` to `'self'`, and add the respondent and date to `resp`. A new initiative gets a new entry in the same shape.

## How it's built

The site is a single static `index.html` with no build step. It loads Plotly.js 2.27.0 from cdnjs and its typefaces from Google Fonts, and it follows the viewer's light or dark setting. GitHub Pages serves it from `index.html` at the root of the `parsons-matrix` repository.

## Sources for the estimates

- [Data Foundation](https://datafoundation.org)
- [AGU Global Data Resilience Convening](https://news.agu.org/press-release/agu-global-data-resilience-convening/)
- [Data Rescue Project](https://www.datarescueproject.org/)
- [NIH GREI](https://datascience.nih.gov/data-ecosystem/generalist-repository-ecosystem-initiative)
- [EDGI](https://envirodatagov.org/about)
- [Public Environmental Data Partners](https://www.screening-tools.com)
- [Open Environmental Data Project](https://openenvironmentaldataproject.substack.com/)

Last updated November 8, 2026.
