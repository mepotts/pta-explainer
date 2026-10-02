# pta-explainer

## Demo

**Live demo:** <https://mepotts.github.io/pta-explainer/>

![Sky map of the pulsar array above the Hellings-Downs curve](docs/screenshot.png)

This is an interactive explainer for how a pulsar timing array detects the nanohertz gravitational-wave background.
It runs in the browser only and is built around the 2023 NANOGrav 15-year Hellings-Downs result.

Claude Code agents wrote the code under automated checks. I set the direction and I am accountable for the result.

## Pulsar Pairs

Pick two of the 67 real NANOGrav 15-year pulsars (or drag an angle slider).
The page shows where the pair lands on the exact Hellings-Downs curve.

## Source Sandbox

The sandbox places one or two illustrative supermassive black-hole binaries on the sky.
It then draws the timing residuals they imprint on six pulsars.

These are example sources and do not represent the real stochastic background.
The 2023 measurement points are not overlaid.

## Code

This repository holds only the built site (generated output).
The source, tests and build configuration are in [`pta-explainer/` in mepotts/astronomy](https://github.com/mepotts/astronomy/tree/main/pta-explainer).

**Stack:** TypeScript, D3, Vite

**License:** MIT

## Testing

**Tests:** 64 Vitest tests, run in CI alongside a type-checked production build.

They cover the Hellings-Downs landmarks (Γ(0°) = 0.5, zero crossing near 49.3°, minimum near 82.5°) with an independent stationary-point check.
They also cover sky-separation geometry, strain and residual scalings and linearity, and a check that averaged antenna patterns reproduce Hellings-Downs.
There are jsdom integration tests as well.

## Data

Pulsar positions derive from the NANOGrav 15-year Data Set (Agazie et al. 2023, Zenodo 10.5281/zenodo.7967584).
It is used under CC-BY-4.0.

This is an independent educational tool. It is not affiliated with or endorsed by NANOGrav.
