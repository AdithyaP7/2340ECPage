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

### **1. Domain Model V1**
The initial domain model created during Sprint 1 focuses on the foundational structure of the WanderSync application, including key classes like `User`, `Destination`, `Dining`, and `Accommodation` with their attributes and relationships.

![Domain Model V1](assets/domainmodelv1.png)

---

### **2. Domain Model V2**
Refined in Sprint 2, this domain model includes additional classes such as `TravelLog` and expands associations to reflect features like travel logging and date tracking.

![Domain Model V2](assets/domainmodelv2.png)

---

### **3. Design Class Diagram (DCD)**
The DCD was introduced in Sprint 3 and incorporates classes for managing dining and accommodation functionalities. It represents relationships such as aggregation, composition, and dependency between classes like `DiningReservation`, `AccommodationBooking`, and `DatabaseManager`.

![DCD](assets/DCD.png)

---

### **4. Sequence Diagram (SD): Login**
This sequence diagram outlines the flow of the login process, including interactions between the user, the `LoginViewModel`, and the `DatabaseManager`.

![SD Login](assets/SD Login.png)

---

### **5. Sequence Diagram / Use Case Diagram: Add Dining Reservation**
This diagram details the interaction for adding a dining reservation, starting from user input to storing the data in the `DiningDatabase`. It highlights collaboration between the `DiningScreen`, `DiningViewModel`, and `DatabaseManager`.

![SD Add Dining Reservation](assets/AddDiningRes.png)
