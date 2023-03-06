
# Project Name: ZSEBRIEF
### About the project
This web app will be designed as a companion for those simulating virtual air traffic control on the VATSIM (Virtual Air Traffic Simulation Network | https://vatsim.net/). VATSIM has 120K active members across the globe and operates an online flight-simulation network where users can fly as a virtual pilot or direct traffic as a virtual air traffic controller with live, real-world weather. This app is designed for the later role: air traffic controller.
Specifically, the app will focus on specific airspace within the confines of the Seattle Air Traffic Control Center (ZSE), which includes most of the Pacific Northwest (see the ARTCC map). The airspace includes a lot of controlled airports and uncontrolled airports., where serving pilots expeditiously requires extensive knowledge of airport characteristics and procedures (which are very dynamic due to weather conditions). This app is meant to quickly provide information about an airport based on live weather conditions so that virtual air traffic services are speedy.

![ARTCC MAP](https://s30121.pcdn.co/wp-content/uploads/2020/01/artcc-map.jpg.webp)

### What the ZSEBRIEF app will provide
ZSEBrief will provide airport information based on real-time weather conditions and for the majority of Class B, C, and D airports (with some Class E airports) in the Seattle Air Traffic Control Center airspace.
The app will provide these key features to help ease their workload.
-	Information about the winds and visibility at the airport and what runway should be used based on calm and non-calm wind conditions.
-	Information about airport field elevation, as well as traffic pattern direction and elevation for both light, turbine-powered, and heavy aircraft.
-	Information about whether Air Traffic Control (ATC) services should be offered for a specific airport based on real-world operating hours.
-	Information about the departure procedures and how to issue an IFR clearance based on the departure type.
-	(Bonus) Ability for certain users to edit airport information.
-	(Bonus) Ability to add traffic currently at an airport to a list; list will indicate time elapsed and help controller prioritize order of services.

### Dependencies
-	Read/write to various “tables” in Firebase Realtime Database.
-	API calls to AVWX (https://account.avwx.rest/)  for live weather information.
-	(Bonus) call to VATSIM real-time data (https://data.vatsim.net/v3/vatsim-data.json) to get list of pilots at covered airports.
-	(Bonus) authentication and roles for making modifications

### Tasks
- [ ] Create airport tables in Firebase Realtime Database.
- [ ] Read master list of airports to the page.
- [ ] Allow user to expand airport to get more information.
- [ ] Establish API call to AVWX and Firebase to get additional airport detail.
- [ ] Create and implement logic for handing errors where certain information is not available.
- [ ] Create and implement logic for showing preferred winds based on conditions.
- [ ] Create and implement logic for calculating whether air traffic control services are available at a given airport.
- [ ] Simplify code and eliminate redundancies.
- [ ] Work on styling and presentation of information.
- [ ] Establish prop types and error handling methods.

(Bonus)
- [ ] Edit / modify airport information.
- [ ] Show pilots at airports utility:
- - [ ] Add lat/long to airport information.
- - [ ] Determine user’s distance from airport by their current lat and long.
- - [ ] Ability to select the pilot, which will add them to a list.
- - [ ] List shows order pilot was added and time elapsed.

### Plan
Prior to 2/27: 
-	Develop airport databases for project (complete)

2/27-3/6:
-	Create react app (complete)
-	Create collapsible user-interface to expand and collapse an airport for more airport detail (complete)
- Connect to firebase database, read, and display information (complete)
-	Connect to airport weather, read and display information (complete)
-	Develop logic to show runways based on weather conditions (in progress)

3/7-3/13:
- Develop logic to show which airports currently have air traffic control 
- Stylize interface
- Simplify code and eliminate redundancies
- Create and implement logic for handling errors (need help here)
- Work on edit/modify functionality

3/14-3/20:
- Work on bonus (show pilots at airports utility)

### Wireframe
https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&edit=_blank&layers=1&nav=1&page-id=vzbuqgKXrLOqEcd3-EA0&title=ZSEBrief.drawio#R%3Cmxfile%20pages%3D%222%22%3E%3Cdiagram%20name%3D%22ZSEBrief%20-%20Airport%20Status%22%20id%3D%22fD9Mnr9-ihHbanxo90jB%22%3E3Zhdb5swFIZ%2FDZeVAANJLtukS7Wlraa0qtY7FxzwajAxZiT99TsGE6AwbWvzUfUiinmP8cdzjn2MDTSNN3OB0%2BiaB4QZthlsDDQzbNtykAN%2FStlWyhh5lRAKGuhKjbCkL0SLplZzGpCsU1FyziRNu6LPk4T4sqNhIXjRrbbirNtrikPSE5Y%2BZn31gQYy0rNwzUa%2FIjSM6p4tU1tiXFfWQhbhgBctCV0aaCo4l1Up3kwJU%2FBqLtV7X%2F5g3Q1MkET%2BywtB5tOLp3n2Ev4Mne%2F3xeNiIs50K78wy%2FWEF7fzWz1gua0pCJ4nAVENmQa6KCIqyTLFvrIW4HfQIhkzeLKg2B9Y3QsRkmxakh7onPCYSLGFKtpa49VBUyMsGg9YtRa16Htaw9rp4a7hhgsUNJr%2FwGT3MJ1TkXIhQZxCzMOfMYKmzUa%2BwTF5H0fMaJhAmZGVPAhWyxn3uI7QMbmiT8kV9ocTc%2FV6XKe5KCdom4%2F3i3v4u6Pv5bgPcG9c6M6hwI0%2BZUC6LjpxQI4%2FJVevPt2cjKvVT%2BANwWUex7gc%2FlJimZ18te%2FORhofMvv7pGceFV8%2FsT8QOLgRoXpLAjVjQVYE9k5VFnlS4O0HBDk6Och%2BJp8RmKPMBSkhcp8EUP547JyBQ9CR2Tk9dgse0uTkqLzxB8vO1qRPiibPBjrvZA612%2BXvjLQAZ1FZVz2sKGNTzrgoG0KBS8aBA3omBX8mLcvYfkKed5BcMxmAP5Rq0KHg155uwe8hhm%2FcVBV9wbPsKDG6S7d1jI4mPU7OACb3YJgGPql3MdreE69xgkOVaPYWpnvAaZt%2Fjzr3QFFnrZ9v1pffXs7WX38U2yskriI8cEFh2B5Tx7kITF5YHewqZcXLD5yGpbfOeW04y8q7JeWFSbqp3tLmup2MMOJLmoRqIvCTlClHkU0KR4FMtazMPKn7gwlVXXaHAXJ7bK%2FcC46QXR92d5GEJ%2BTVlqOlDKJADQ7N3ObpjkNEzNTiHI4VDr5fsfLeKaJBQOA8fNGNsH0sQvvVecTq59TBzeoNqxAemzuz0ta6eUSXvwE%3D%3C%2Fdiagram%3E%3Cdiagram%20name%3D%22ZSEBrief%20-%20Departure%20Manager%22%20id%3D%22vzbuqgKXrLOqEcd3-EA0%22%3E7VrbUts6FP2aPHLGtnzLIySUTksKJVCmfTkjbCVWkaUcWSGBr69ky%2FFFpgca4sCUvFjZUiR5rbX31iUDMErXJxwukgmLERk4VrwegPHAcWwXuPKhLPeFJQR%2BYZhzHOtGlWGKH5A2Wtq6xDHKGg0FY0TgRdMYMUpRJBo2yDlbNZvNGGmOuoBzZBimESSm9RrHItFv4VmV%2FSPC86Qc2bZ0TQrLxtqQJTBmq5oJHA%2FAiDMmilK6HiGiwCtxmY8f1sMvNDz68f16tLQ%2F%2BAfjTwdFZx%2Be85PNK3BExct27RRd30Gy1Hidnp2c6fcV9yWInC1pjFRH1gAcrRIs0HQBI1W7krKRtkSkRH6zZfGJs9VvdYe4QOsaV3r2J4ilSPB72UTXlpRpIZa0rCpW7dKW1Bj1tQ1qIc03HVdgyYLG6xnYAQO7L1IKUt4cRreYzgfgUPkNkkiIJZc%2BIEW%2B5AoVot6KNhtvBTkkeE5lmaCZ6I8B33ENCgLQJwWuQcHl08B%2Fy7DL6LVn2D0D9lGBrTT%2BuDq9ko9LnKJXGkb%2BMI64u0LTtg04T9kc09cJnx%2B%2BNvg6chimt0UAOMR8wbjS5VRAscy2wzSGWZK37THNDTvw7XJ2sDN8zSBb4TsuA6wsTyCViyn%2BghDPMCEjRhjPOwKxh8LYlfZMcHaLajWhcwN8f4ekONb%2Fs%2BLtiJXLI7pyLxIwPPu2iL9dWHiyetBrvTopA8eHqUKT3mTqIaUfcThT2h8EchCritGVVxQ1RbC2zijBdMuovZ%2BUGPiewceGo5dOiQeTn0569Xn4%2FRr8%2FDpZUX7sXnfy0cJR7h8WqhhxlmX7C%2BAbXErsQlPLuwowndCZ6e9vlrI%2FNBfV%2FUrZzKdvRsrWcL9SNhfGf7OUQ7BvKftvVsqhu2cpB%2B9Sbqz39i3l8M1KeWjvWcrDHUg5P0BSmlW7INV7iumWu8uWsl%2FP5qflC8Cy9%2BwL9i52Pw1GvR4Ync1mThR1MRr7N77XJ6OBuQXomdFdbAIajAZ9MBpGqJvRm9BzPas%2FRl0Q7JvRJ2wjoiW%2F2xz2IBofqvs%2BlcAIzDIcNaFv8vQ8HFHcuCQ0UazB1HWMU9o4IlDgu%2BbVYhd0eoRzhnOBapJAe6%2FntdDP2JJHSP%2BqIsDoyG0dR4E2jQLyORJGRxJgeF9rtlANsscn7LltWVm%2Fn1cr9YOw0V4WihlUstpw8CSljdLL6cnD%2FeTfj8kZuDj%2FDM%2BnX7uPwohyz0Qy5M%2BLZWJhmbF8upUG%2Ff%2BWrKw4yPLbaxUthot18StdXfYTEazvjSyo9EcgzSMNJuqRsrv8pkmwWvTRI8tXKwZvTkia67NsOYh0ftH0gmZkoUwO3wxD2pTJEJZfg4296tslk%2BFsfOA8Fujk9PmM5C6Y4DhGdEu3e3r42gj4Nzt5O%2BjwzNDdPn51qurlT0GMpGDlH83fVPebMaLm1U4tm7acCRmCmEpCbk5t8Y8L6x%2FbtV3HBp4v0zmwLd%2FdJV120PTzrnTTwZbzAtmmky3zLv6drUfZcu2OBXyfbJk3Su9s1dgKm2wFHUcPfbLVeajZQ36lOSZq0VXm1XrKnXGWvmfZZ24S7NbyzOvY93VpK3i%2BtuTX6q9xxVKv%2BoMhOP4F%3C%2Fdiagram%3E%3C%2Fmxfile%3E
