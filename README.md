# Vehicle Routing Problem with Time Windows (VRPTW) Solver

## Introduction
The Vehicle Routing Problem with Time Windows (VRPTW) is a complex optimization challenge that involves determining the most efficient routes for a fleet of vehicles to deliver goods to various locations within specific time frames. This project implements a solution to the VRPTW using Google OR-Tools, a powerful suite of optimization tools developed by Google.

## Overview
The VRPTW is an extension of the classic Vehicle Routing Problem (VRP). The key difference is the addition of time windows, which are constraints that specify the time range within which a delivery or service must be made. This adds a layer of complexity to the problem, as the algorithm must now consider not only the shortest or most cost-effective route but also the scheduling of deliveries to meet these time constraints.

## Algorithm and Solution
To solve the VRPTW, this project utilizes the Google OR-Tools library, which provides efficient algorithms for routing problems. The core of the solution is a constraint programming model that captures the various requirements of the VRPTW, such as vehicle capacity, route length, and time windows. The model is then solved using a combination of heuristics and exact algorithms to find optimal or near-optimal solutions.

## Visualization
The results of the optimization are visualized using two libraries:
- **Matplotlib**: A plotting library for Python which provides a way to visualize data in a 2D format.
- **Folium**: A library that makes it easy to visualize data that’s been manipulated in Python on an interactive leaflet map.

## Python Code and Libraries
The project is implemented in Python, leveraging the following libraries:
- **Google OR-Tools**: Provides the optimization algorithms used to solve the VRPTW.
- **Matplotlib**: Used for creating static, animated, and interactive visualizations in Python.
- **Folium**: Used for map visualization, allowing for the interactive display of the routes on a map interface.

## Getting Started
To run this project, you can use Google Colab on cloud. To run this project locally make sure you have a proper python environment configuration for running the project.

## Code Explanation
We have four different functions

1. create_data_model():
    * This function initializes and returns the data required for solving the Vehicle Routing Problem with Time Windows (VRPTW).
    * It includes the distance matrix between locations, time windows for each customer, the number of vehicles, and the depot location.

2. print_solution(data, manager, routing, solution):
    * This function prints the solution of the VRPTW problem to the console.
    * For each vehicle, it prints the route taken, including the sequence of customers visited, their respective time windows, and the total time of the route.
3. plot_routes(data, manager, routing, solution):
    * This function visualizes the routes generated by the VRPTW algorithm using Matplotlib.
    * For each vehicle, it plots the route on a 2D graph, with nodes representing customers and lines representing the path taken by the vehicle.
4. plot_map(data, manager, routing, solution):
    * This function visualizes the routes generated by the VRPTW algorithm using Folium maps.
    * It generates an interactive map where each vehicle's route is displayed as a polyline on the map. Each customer's location is marked with a marker, and clicking on the marker shows additional information about the customer.
5. main():
    * This is the main function that orchestrates the entire process of solving the VRPTW problem and visualizing the results.
    * It calls the create_data_model() function to initialize the problem data.
    * It sets up the routing model using OR-Tools, solves the problem, and obtains the solution.
    * Finally, it prints the solution to the console and visualizes the routes using both Matplotlib and Folium maps.

## Conclusion
This VRPTW solver demonstrates the power of optimization tools in solving complex logistical problems. By integrating Google OR-Tools with Python’s visualization libraries, we can not only find efficient routes but also present them in a clear and interactive manner.

## Contribution
If you have any questions about this solution, please contact me at <21cs2011@rgipt.ac.in>
***Mann Bajpai***