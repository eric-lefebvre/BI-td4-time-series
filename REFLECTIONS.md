## Stage 0 — Framing (CM3: Modern Data Acquisition, CM4: Automated Pipelines)
**Reflection 1.** The synthetic-data plan was reasonable-sounding and wrong. Before
reading further: what would you have had to do to *check* whether real historical
CO2 data was available, instead of just assuming it wasn't? Name one concrete
action. (This is CM3's acquisition-planning discipline in miniature: an assumption
about what data is available is itself a claim that needs checking, not something
to design around unverified.)

Send one test request to the API with `past_days=90` (or just read the `past_days` parameter in the Air Quality API docs) and look at whether it really returns 90 days of hourly values. It takes five minutes, way less than designing a whole synthetic data generator around an assumption nobody checked.

## Stage 1 — Collection (CM3: acquisition patterns, provenance)
**Reflection 2.** Before running the script below: the location is fixed to Le Mans
(48.0061, 0.1996). Based on what you know about seasons and plant growth, do you
expect atmospheric CO2 there to be *rising*, *falling*, or *flat* over the last 90
days from today? Write your prediction down before you look at your own output —
you'll check it in Stage 3.

I expect CO2 to be rising. The last 90 days go from mid-August to early November: plants absorb CO2 during summer, so the minimum is around late August/September, then it goes back up in autumn when leaves fall and decompose and people start heating. I expect a small slope (a few tenths of ppm per day) with some day-to-day noise from the weather.
