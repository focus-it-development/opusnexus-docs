# OpusTables known issues

These are the current Beta limits. Most are on the plan.

1. Windows x64 only for now. A Mac version is planned.
2. Functions beyond SUM, AVERAGE, and COUNT (such as IF and lookups) are not supported yet. Formulas that use them keep the value Excel saved until something they depend on changes, then show `#NAME?`. IF, MIN, MAX, and ROUND are planned next.
3. No charts, merged cells, conditional formatting, comments, drop-down lists, or fill handle yet. Files with these open as a copy by default. Merged cells are planned next.
4. Cut and paste moves the cells but does not update formulas elsewhere that pointed at them.
5. Fonts from opened files are kept in the file but shown in Roboto.
6. No printing beyond PDF export.
7. Filters do not re-run on their own after editing. Apply the filter again to refresh it.
8. Beta installers are not code signed, so Windows shows a SmartScreen warning the first time. See [Getting started](getting-started.md).

Found something not listed here? Open an issue in this repository or email beta@opusnex.us.
