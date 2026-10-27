# Fuel Friend by Washly's

A free page that helps South African motorists spend less on fuel: when to fill up around official price changes, diesel prices by station in 11 cities, which rewards cards each brand accepts, and dated fuel-sector news.

Brought to you by [Washly's](https://www.instagram.com/washlyscarwash/), a mobile car wash in Gqeberha.

## How it works

It's a single static page, `index.html`. All figures live in the `const DATA = {...}` block at the top of its script, and each one carries its date and source. The page warns visitors when its prices are out of date.

## Data sources

- Official petrol prices and diesel wholesale prices: Department of Mineral and Petroleum Resources, via PetrolPrice.co.za
- Price forecasts: Central Energy Fund data as reported by iWantFuel, BusinessTech and others
- Station diesel prices: myTank (reported by drivers and station owners)
- News: each item links to its source

## Hosting

Served by GitHub Pages from the root of the `main` branch.

## Settings you can change

In `index.html`:

- **Visitor counting:** near the top, put your GoatCounter code between the quotes in `const GOATCOUNTER_CODE="";` (for example `"fuelfriend"` if your dashboard is fuelfriend.goatcounter.com).
- **Contact email:** in the `DATA` block, `contact:{email:""}`. While it's empty, the booking, fleet and advertising buttons point to Instagram.
- **Promo:** `promo:{code:"FUELFRIEND10",offer:"10% off your first wash"}`. The Washly's card only shows when the visitor picks Gqeberha.
- **Driving distances:** in the page script, `const ROUTING={orsKey:""};`. Paste a free openrouteservice.org API key between the quotes for real road distances and route lines. While it's empty, the "Use my location" finder estimates driving distance from straight-line distance and says so.
- **Sponsor:** `sponsor:null`. To show a paid placement, replace `null` with `{name:"Business name",text:"One line about the offer",url:"https://...",cities:["gqb"]}`. Leave out `cities` to show it everywhere. It's always labelled "Sponsored" and never changes the price order.

## Security notes

- **Map library:** Leaflet 1.9.4 is served from this repository (`vendor/leaflet/`) rather than an outside server, so its code can't be swapped without a change here.
- **Price check:** reported station prices are set aside, and named under the station list, if they are outside R20 to R50, more than R4.50 below or R4.00 above the city's middle price, or more than R2 below the official wholesale price. This stops a typo or a bad data feed from becoming the "cheapest" station.
- **Account:** keep two-step verification on for the GitHub account that owns this repository.

## Location and privacy

The "Use my location" button asks the browser for the visitor's position. It is used only on the visitor's device to find nearby stations and is sent once to openrouteservice.org to measure driving distances (only when a key is set). Fuel Friend never stores or logs it.
