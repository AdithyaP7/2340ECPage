---
layout: default
title: Design & Architecture
---

# Design & Architecture

## Overview
The architecture of WanderSync is built on the **Model-View-ViewModel (MVVM)** pattern to ensure a clean separation of concerns and scalability.

### Design Patterns Used
1. **Singleton Pattern**
   - **Purpose**: Ensures only one instance of a class is created, providing a global point of access.
   - **Implementation in WanderSync**:
     - Applied in Sprint 2 to manage the `DatabaseManager` for all interactions with Firebase. This ensures consistent and efficient handling of user and travel data.

2. **MVVM**
   - **Purpose**: Ensures efficient data binding between the UI and the underlying logic.

3. **Observer Pattern**
   - **Purpose**: Establishes a subscription mechanism to notify dependent objects when changes occur.
   - **Implementation in WanderSync**:
     - Introduced in Sprint 3 and expanded in Sprint 4 to update the UI in real-time when new data (e.g., dining reservations or community posts) is added to the database.
     - Used to reflect immediate changes in the Travel Community and collaboration features.

4. **Strategy Pattern**
   - **Purpose**: Defines a family of algorithms, encapsulates each one, and makes them interchangeable at runtime.
   - **Implementation in WanderSync**:
     - Employed in Sprint 3 to sort and filter dining and accommodation reservations. Users can sort by time, date, or type of reservation.

5. **Factory Method Pattern**
   - **Purpose**: Provides an interface for creating objects while allowing subclasses to specify the type of object to create.
   - **Implementation in WanderSync**:
     - Mentioned in Sprint 4 to streamline the creation of travel posts. Used to generate different types of entries (e.g., accommodations, dining reservations) based on user inputs.

## UML Diagrams
### Design Class Diagram
Below is a UML diagram showcasing the relationships and structure of the core components in the application:

![Design Class Diagram](assets/uml_diagram.png)

### Sequence Diagram
Here is a sequence diagram illustrating how a user interacts with the system to book a trip:

![Sequence Diagram](assets/sequence_diagram.png)

These diagrams provide a clear visual representation of the application's design and how its components interact.
