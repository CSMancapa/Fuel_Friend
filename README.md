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
- **Sponsor:** `sponsor:null`. To show a paid placement, replace `null` with `{name:"Business name",text:"One line about the offer",url:"https://...",cities:["gqb"]}`. Leave out `cities` to show it everywhere. It's always labelled "Sponsored" and never changes the price order.
