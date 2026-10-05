# Online UPS Interactive Site

Static GitHub Pages package for the DAC office Online UPS scenario dashboard.

## Publish free with GitHub Pages
1. Create a new public GitHub repository.
2. Upload all files and the `assets` folder from this package to the repository root.
3. Open **Settings > Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. GitHub will show the published site link after deployment.

## Data model
- UPS rating: 5,000 VA, power factor 0.8, rated real power 4,000 W.
- Battery model: 48 x 12 V x 5 Ah = 2,880 Wh nominal per UPS.
- Normal baseline: UPS 1 = 1,540 W; UPS 2 = 393.4 W.
- All-on totals: UPS 1 = 4,391 W; UPS 2 = 4,803.4 W.
- Backup time is a scenario estimate. Adjust derating in the Summary view and verify operational runtime on the physical UPS display.

## Controls
- Click directly on an existing numbered circle in each floor map.
- Green means ON. Blue means OFF. Amber outline means optional.
- Protected server racks and ACUs require Maintenance override before switch-off.
- State is saved locally in the browser.

## Edit data or hotspot positions
Open `data.js`. Each device has `x` and `y` percentages. These place the transparent clickable hotspot on the existing numbered circle without changing the floor map.

## Live UPS impact by floor
- Level 7 displays the live total for UPS 1.
- Level 9 displays UPS 1 and UPS 2 side by side.
- Level 11 displays the live total for UPS 2.
- Every switch operation displays before, after, and watt change for the affected UPS.
- The UPS Dependency tab groups connected equipment by UPS and floor.
