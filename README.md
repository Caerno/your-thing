# Your Thing · Кем быть

An adaptive career test that runs entirely in the browser. Three questionnaires feed one joint Bayesian profile, and 923 O*NET occupations are placed in the same space. Each occupation opens with tabs: the O*NET description, ESCO occupations from the official crosswalk, and (Russian version) similar occupations from the Russian Ministry of Labour directory.

- English: https://caerno.github.io/your-thing/
- Русская версия: https://caerno.github.io/your-thing/ru/

## How it works

- **Instruments.** A 48-item RIASEC interest bank, the ten-item TIPI (Big Five) and the twenty forced-choice pairs of Klimov's DDO.
- **Model.** One joint Gaussian over eleven latent scales: six interests and five personality traits. Prior correlations and the RIASEC and TIPI item parameters are estimated on 107,256 people who took both tests (graded response model, coarse classical calibration).
- **Updating.** Each answer updates the whole profile by expectation propagation. The next item is the one with the largest expected reduction of uncertainty in the six interest scales.
- **Matching.** Occupations are ranked by distance in the interest space, with each axis weighted by how certain the estimate is.

## Limits

- DDO options are mapped onto RIASEC by content and are not calibrated.
- The Russian wording of the TIPI items is a working translation, not a validated adaptation.
- Occupation titles are in English in both versions.
- Ministry of Labour matches are chosen automatically by title within the same ISCO group and can be wrong.

## Privacy

No backend and no analytics. Answers are kept in the browser's local storage and are not sent anywhere.

## Sources

- RIASEC items and raw response data: openpsychometrics.org, collected 2015–2018; items after Liao, Armstrong & Rounds (2008).
- TIPI: Gosling, Rentfrow & Swann (2003).
- DDO: E. A. Klimov.
- ESCO classification, © European Union; crosswalk ESCO → O*NET-SOC 2019 by the O*NET Resource Center.
- Occupation directory of the Ministry of Labour and Social Protection of the Russian Federation (spravochnik.rosmintrud.ru).
- This page includes information from the O*NET 30.0 Database by the U.S. Department of Labor, Employment and Training Administration (USDOL/ETA). Used under the CC BY 4.0 license.

## Contact

Profiles and comments are welcome at kirsanov.dima@gmail.com.
