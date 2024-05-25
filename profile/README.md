## Naviqore

Public transportation systems play a crucial role in urban mobility, connecting millions of people daily. Efficient
routing algorithms are essential for optimizing transit journeys, minimizing travel time, and enhancing user experience.
In this Master thesis, we delve into the challenges of public transit routing and explore innovative approaches to
address them.

## Motivation

The motivation behind our thesis lies in addressing several key challenges:

1. **Open Data**: In recent years, a growing number of public transit agencies have started to publish their schedules
   in the open standard GTFS (General Transit Feed Specification) as open data [1]. Maintaining a public transit
   schedule is a resource-intensive task, making it previously inaccessible for small companies or private individuals
   to access or generate such datasets. Working with these large and complex datasets poses interesting challenges
   concerning efficient data structures and processing approaches.

3. **Complexity**: Routing in public transit systems is inherently complex due to the time-dependent nature of the
   network. The schedules of public transit services are not static; they vary based on time of day, day of the week,
   and other factors. This time-dependency adds a layer of complexity to the routing process, making it a challenging
   problem to solve efficiently.

4. **Performance**: Traditional graph-based transit routing algorithms often struggle with large-scale networks,
   resulting in time-consuming requests. The RAPTOR (Round-based Public Transit Routing) algorithm, known for its speed
   and accuracy, offers a promising solution [2].

Implementing a public transit service integrates various aspects of the MAS Software Engineering curriculum, including
architecture and design, algorithms and data structures, project automation, communication in distributed systems,
testing, and containerized deployment. Working in a team with an agile, iterative setup provides an exciting opportunity
to address these challenges effectively and learn from mistakes during the software development process.

## Approach

Our approach involves the following key components:

1. **GTFS**: We use public transit schedules in the General Transit Feed Specification (GTFS) format as data
   source. GTFS provides a standardized format for transit schedules, including static information (such as stop times,
   routes, and trips) and eventually real-time updates.

3. **RAPTOR Algorithm**: The RAPTOR algorithm, based on time-expanded networks, efficiently computes transit routes by
   considering time-dependent constraints.

4. **Public Transit Service**: This integration layer adds abstraction between the publicly visible interface and the
   core components, such as the routing algorithm and schedule data source. This will allow for exchanging those
   components without interfering with any outside dependencies on the service.

5. **Web Application**: Around the core routing functionality, we develop a simple web application. The frontend will
   allow users to explore schedules, query connections, and assess accessibility. The backend continuously updates the
   static schedule.
