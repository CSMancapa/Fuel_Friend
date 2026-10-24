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
