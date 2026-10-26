# Response to supervisor comments: continuing declines (Q1 and Q2)

## 1. "2 pages"

Both questions now fit on one page each: two pages in total.

- `outputs/Q1_Continuing_Declines.pdf`
- `outputs/Q2_Decline_Concentration.pdf`

Regions, habitats and ecological groups are now combined on the single Q2 page.

## 2. "Seems to be population, not breeding"

Agreed. The previous version measured where a species was recorded, which reflects distribution and population, not breeding. Both questions are now rebuilt on breeding evidence.

- **Measure.** Breeding share: of the Atlas surveys that recorded a species, the share with breeding evidence. This uses surveys only, as the team agreed.
- **Fair comparison.** Each species is standardised to the same mix of months in every period. It is compared with the typical species, because breeding was recorded less often overall over time.
- **Data sources.** DES (2021–2025) is not pooled with the Atlas, following the agreed rule.

The results change materially.

- **Q1.** 13 native species are still declining in breeding. 6 are colonial waterbirds: Intermediate, Great, Little and Cattle Egret, Straw-necked Ibis and Nankeen Night-Heron. 7 are other species, mostly woodland birds, including Fuscous Honeyeater, White-throated Gerygone and Yellow-rumped Thornbill.
- **Q2.** Breeding fell most inland from 1977–1999 to 2000–2009, then most on the tablelands from 2000–2009 to 2010–2020. Insect-eaters are the only ecological group clearly below typical.

## 3. "Generic speculation on changes"

Each cause is now tied to a pattern in our own results, or to a check against our other analyses.

- **Colonial waterbirds.** Their breeding stayed low in 2010–2020 despite the 2010–12 floods. That points to less water reaching colony wetlands, or fewer Atlas visits to colonies, rather than drought. It can be tested against aerial waterbird colony counts.
- **Drought.** Eight species fell during the Millennium Drought and recovered afterwards, which shows what a drought response looks like. The 13 continuing decliners did not recover, so drought alone does not explain them.
- **Noisy Miners.** These were ruled out for the woodland decliners. In the "Hidden Pressures" matched comparison, their breeding odds with miners were 0.90–1.13 times those without miners, which is about the same.
- **Inland pattern.** Inland breeding dropped in the drought decade and recovered after it, at +6% against the NSW trend. This can be tested directly with the team's rainfall analysis.
- **Tablelands pattern.** The tablelands drop was already visible in 2010–2016, before the 2017–19 drought. That points to a slow pressure, such as dying paddock trees and dieback, rather than a single drought.

These remain hypotheses and are labelled as speculation on the pages.

## 4. "Why so few blocks?"

The previous map had only 41 large cells, about 100 km across. That method needed the same grid squares surveyed at least four times in each of three periods, which left only 432 squares.

The breeding map now uses cells about 50 km across. A cell needs at least 10 expected breeding records, comparing 1977–1999 with 2000–2020. That gives 222 cells.

Each cell compares observed recent breeding records with the number expected if every species kept its earlier breeding share. This keeps each cell's own species mix fixed.

## 5. "Why those time spans?"

The previous spans of 1977–1990, 1991–2005 and 2006–2020 were equal thirds of the Atlas, with no ecological reason behind them. They are replaced with spans tied to the team's agreed periods.

- **1977–1999.** The team's agreed early period.
- **2000–2009 and 2010–2020.** The team's agreed recent period, split at 2010. This tests whether a decline is still going. 2000–2009 covers the Millennium Drought, and 2010–2020 covers the period after it. Splitting here separates species that recovered when the drought ended from those still declining.

The Atlas ends in March 2020. DES 2021–2025 can be used later to check whether the continuing decliners keep falling, using within-DES comparisons only.

## Still to confirm

- **Trait table.** The habitat, diet and movement groups come from a provisional trait table (`species_traits_provisional.csv`). It should be checked against the team's `Species-Traits-table.tsv`.
- **Small recent samples.** Several continuing decliners have fewer than 10 breeding records in 2010–2020, so their size of decline is uncertain. Their direction is supported by the 95% ranges.
