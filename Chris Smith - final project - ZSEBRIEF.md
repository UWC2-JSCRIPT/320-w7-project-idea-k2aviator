
# Project Name: ZSEBRIEF
### About the project
This web app will be designed as a companion for those simulating virtual air traffic control on the VATSIM (Virtual Air Traffic Simulation Network | https://vatsim.net/). VATSIM has 120K active members across the globe and operates an online flight-simulation network where users can fly as a virtual pilot or direct traffic as a virtual air traffic controller with live, real-world weather. This app is designed for the later role: air traffic controller.
Specifically, the app will focus on specific airspace within the confines of the Seattle Air Traffic Control Center (ZSE), which includes most of the Pacific Northwest (see the ARTCC map). The airspace includes a lot of controlled airports and uncontrolled airports., where serving pilots expeditiously requires extensive knowledge of airport characteristics and procedures (which are very dynamic due to weather conditions). This app is meant to quickly provide information about an airport based on live weather conditions so that virtual air traffic services are speedy.
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
