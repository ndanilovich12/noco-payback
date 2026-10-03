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

Estimates get tighter as better data comes in. With only building type and size it's ±35%. A utility bill brings that to ±20%, and a technician walkthrough to ±10%.

## Built with

Plain HTML, CSS and JavaScript in one file. No frameworks and no build step. To run it, open `index.html` in a browser.

## Heads up

The customers, addresses and contacts are made up. The customer stats and anything marked ◊ are placeholder numbers, not NOCO's real data.
