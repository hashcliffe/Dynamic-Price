# Dynamic-Price
Dynamic Pricing for Urban Parking Lots

This project implements a dynamic pricing model for urban parking lots using real-time occupancy data and contextual information. The goal is to optimize parking prices based on demand, traffic, time, and other dynamic factors.

Features

* Calculates occupancy rates from historical parking data
* Computes average occupancy using 1-hour tumbling window
* Applies a dynamic pricing formula based on:
* Time of day
* Traffic condition
* Vehicle type
* Queue length
* Special event indicator
* Implements logic using Pathway, a real-time dataflow framework
* Visualizes or collects output through CSV export

How It Works

* A small sample (e.g., 20 rows) is read using pandas for performance.
* Data is converted into a Pathway Table.
* Timestamps are created and converted to datetime.
* Occupancy rate is calculated.
* A 1-hour window average is computed using pw.temporal.tumbling().
* A dynamic pricing function determines hourly rate per vehicle.
* Output is exported using debug() snapshot to pricing_debug_output.csv.

Tech Stack

* Python 3.12
* Pathway for data processing
* Pandas for sampling
* Panel & Bokeh for visualization

