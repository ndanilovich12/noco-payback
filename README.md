# NOCO Payback

An interactive demo of an energy-savings sales tool for commercial buildings in Western New York. It shows two views of the same deal side by side: the customer's mobile app and the provider's desktop console. Both are driven by one shared calculation engine, so a change in one view updates the other.

**Live demo:** https://ndanilovich12.github.io/noco-payback/

## Background

Built as a prototype for NOCO through UB AI for Good, a University at Buffalo program in which student teams build AI solutions for partner organizations. This was a team project; I led the design and development of the prototype.

## What it does

**Customer app (phone)**

- Confirms the building from its address and shows what similar buildings save
- Takes a utility bill photo to replace typical-building estimates with real usage
- Books a technician visit
- Presents ranked upgrade offers with savings, incentives, net cost and payback

**Operator console (desktop)**

- Customer list with building details and recent activity
- Technician walkthrough that records what was found on site
- Upgrades ranked by payback, with the full math behind every number
- Offer builder that packages upgrades and incentives for the customer

## The payback engine

One set of functions estimates each upgrade from the building's size, shape, envelope, heating system and energy use:

| Upgrade | Basis of the estimate |
| --- | --- |
| Insulation | Wall area and R-value change over heating and cooling degree-days |
| LED lighting | Lighting share of electric use by building type |
| Heating | Heat pump or high-efficiency gas, from the existing system's efficiency |
| Solar | Usable roof area, capped at annual electric use |

For each upgrade the engine returns energy saved, annual cost savings, project cost, incentives, net investment, simple payback and ten-year value. Every result carries a plain-language explanation and the step-by-step arithmetic, which the console can show on request.

Estimates also carry a confidence level that tightens as better data arrives:

| Data available | Confidence | Range |
| --- | --- | --- |
| Building type and size only | Low | ±35% |
| Utility bills | Medium | ±20% |
| Technician walkthrough | High | ±10% |

## Tech

- A single `index.html` file: HTML, CSS and vanilla JavaScript
- No frameworks, build step or dependencies
- Light and dark themes
- Responsive layout that collapses to the phone view on small screens

## Run it locally

Download `index.html` and open it in a browser.

## Notes

This is a demo. The customers, addresses and contacts are fictional, and the customer statistics and any assumption marked ◊ are placeholders rather than real program or company data.
