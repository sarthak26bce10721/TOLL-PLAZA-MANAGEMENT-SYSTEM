# Problem Statement: Highway Toll Plaza System

## 1. Problem Description
At highway toll plazas, managing vehicles manually with paper receipts or mental calculations causes several real-world headaches:
* **Calculation Mistakes:** Cashiers often have to quickly calculate different rates for cars, buses, and trucks, along with extra charges for return journeys. Doing this by hand during rush hours leads to billing errors and slow lines.
* **No Quick Vehicle Counting:** Shift supervisors have a hard time knowing exactly how many trucks or cars passed through their specific booth during the day.
* **Delays for Emergency Vehicles:** Ambulances and VIP convoys sometimes get stuck or mistakenly charged because there isn't a quick, automatic way to flag their number plates.
* **Cash Drawer Risk:** If cash piles up in the booth drawer without anyone noticing, it becomes a security risk. Staff need a clear reminder when it is time to transfer money to the main office safe.

## 2. Project Goal
The goal of this project is to build a simple, reliable command-line tool in Python that handles toll collection quickly and accurately:
* Show standard single and return rates for common vehicle types (Car, Bus, Truck).
* Generate tickets instantly and calculate exact billing amounts.
* Automatically detect emergency and official vehicles (`AMB` and `VIP`) and let them pass for free.
* Keep a live running count of vehicles that pass through the counter.
* Save all transactions and warn the operator when total cash collected crosses the safety limit.

## 3. Target Users
* **Toll Booth Operators:** To quickly check vehicle types, issue tickets, and take payments.
* **Shift In-Charge / Supervisors:** To check shift totals, view traffic counts, and make sure cash isn't overflowing in the counter.

## 4. System Structure
To keep the code clean and follow modular programming practices, the project is divided into 6 straightforward files:
1. `booth.py` — Tracks vehicle counts passing through the lane.
2. `pricing.py` — Stores rates and calculates single vs. return ticket prices.
3. `records.py` — Stores transaction receipts and totals the collected cash.
4. `rules.py` — Checks number plates for ambulance and VIP exemptions.
5. `reports.py` — Holds fixed alert messages and drawer cash limits.
6. `main.py` — Runs the main user menu and coordinates all actions.