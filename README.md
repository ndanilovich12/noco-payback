# NOCO Payback

Live demo: https://ndanilovich12.github.io/noco-payback/

A prototype my team built for NOCO through UB AI for Good. I led the design and the build.

The idea: a small business owner in Western New York should be able to find out what energy upgrades would save them, and what they'd cost after incentives, without waiting weeks for a quote. The demo shows the customer's phone app next to NOCO's desktop console. Both run off the same calculation code, so when a technician logs something in the console, the customer's numbers change too.

## How it works

On the phone, a customer confirms their building, snaps a utility bill, and books a technician visit. After the visit they get offers showing yearly savings, incentives, what they'd pay, and how long until it pays for itself.

On the console, NOCO staff see the customer's building info, run the technician walkthrough, and build the offer. Every number can be expanded to show the math behind it.

The engine looks at four upgrades:

- Insulation, from wall area and the change in R-value over a Buffalo heating and cooling season
- LED lighting, from the share of electric use that goes to lighting for that building type
- Heating, either a heat pump or high-efficiency gas depending on the current system
- Solar, sized to the usable roof and capped at what the building actually uses

## November 2026 update

This version is the one we presented. It adds a guided demo that walks through the whole process in nine steps, from a free visit to a same-day quote:

- It runs on public data for real Buffalo addresses: NYSERDA electric prices and the City of Buffalo assessment roll.
- AI reads the utility bill photo and the technician's spoken walkthrough. Formulas do the math, so every dollar on the quote can be traced.
- In the demo, 21 of 21 quote inputs are filled in before anyone types.
- The customer picks between two offers on their phone while the console shows what was sent.

Use the Next button or the arrow keys to move through the steps.

## Built with

Plain HTML, CSS and JavaScript in one file. No frameworks and no build step. To run it, open `index.html` in a browser.

## Heads up

Business names, contacts and bills are made up for the demo. The customer stats and anything marked ◊ are placeholder numbers, not NOCO's real data.
