# Dashboard Documentation

## Source File
- `index.html` (single-file dashboard with inline styles and scripts)

## Tech Stack
- HTML5
- CSS3 (inline `<style>`, CSS variables, Grid/Flex layouts)
- Vanilla JavaScript (inline `<script>`)
- Chart.js for data visualization

## External Libraries
- Google Fonts (Inter): `https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap`
- Chart.js 4.4.1 (UMD): `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js`

## CSS Structure
- Theme tokens in `:root` (`--bg`, `--text`, chart/accent colors)
- Base/reset: `*`, `body`, `html`
- Layout wrappers: `.dashboard`, `.top-bar`, `.stats-row`, `.panels-row`, `.panels-row2`
- Reusable panel system: `.panel`, `.panel-header`, `.panel-title`, `.panel-subtitle`, `.panel-body`
- Chart/legend styles: `.chart-wrap`, `.legend`, `.legend-item`, `.legend-dot`, `.legend-line`
- Feature UI groups: stats cards, tariff/rate cards, recommendation cards

## HTML Sections
- Top bar: title, live badge, timestamp, user badge
- KPI cards: Weekly Cost, Usage, Electricity Rate, Gas Rate
- Cost Overview panel (weekly stacked bar)
- Energy Consumption panel (doughnut + breakdown)
- Energy Consumption by Appliance - Hourly (multi-line chart)
- Current Tariff panel
- Recommendations panel
- Rate Trends panel (two sparklines)

## Chart IDs
- `costChart`
- `pieChart`
- `lineChart`
- `sparkElec`
- `sparkGas`

## Data Arrays
- `days`: `['SUN','MON','TUE','WED','THU','FRI','SAT']`
- `hours`: `['00' ... '23']`
- Cost datasets:
  - Electricity: `[6.2, 7.1, 4.38, 8.4, 7.8, 6.9, 5.5]`
  - Gas: `[2.1, 3.0, 2.76, 3.2, 2.9, 2.5, 2.0]`
- Pie dataset: `[32, 26, 19, 23]` (Heating, Fridge, Dishwasher, Oven)
- Hourly series arrays: `heatingData`, `fridgeData`, `dishData`, `ovenData`
- Sparkline datasets:
  - Electricity: `[19.8, 20.1, 20.0, 20.3, 20.2, 20.4, 20.5]`
  - Gas: `[4.0, 4.1, 4.1, 4.2, 4.1, 4.1, 4.2]`

## Notes
- Static demo UI; no backend/API integration in this file.
- Chart defaults are set globally (`Chart.defaults`) for color, borders, and font.
- Layout is responsive through CSS Grid/Flex with fixed chart container heights.
