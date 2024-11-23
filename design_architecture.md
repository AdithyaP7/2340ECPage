---
layout: default
title: Design & Architecture
---

# Design & Architecture

## Overview
The architecture of WanderSync is built on the **Model-View-ViewModel (MVVM)** pattern to ensure a clean separation of concerns and scalability.

### Design Patterns Used
- **MVVM Architecture**: Ensures efficient data binding between the UI and the underlying logic.
- **Singleton**: Used for managing shared resources like the `UserManager` or `TravelManager`.
- **Observer**: Keeps the UI updated with real-time changes in travel itineraries.

## UML Diagrams
### Design Class Diagram
Below is a UML diagram showcasing the relationships and structure of the core components in the application:

![Design Class Diagram](assets/uml_diagram.png)

### Sequence Diagram
Here is a sequence diagram illustrating how a user interacts with the system to book a trip:

![Sequence Diagram](assets/sequence_diagram.png)

These diagrams provide a clear visual representation of the application's design and how its components interact.
