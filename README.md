# Lab #1 - Community Events Management System

## Project Overview
In this lab, you will build a system for organizing community events using Object-Oriented Programming (OOP) principles. The system will include different types of events, community leaders, volunteers, and a cultural hub. This lab will help reinforce your understanding of OOP concepts, including inheritance, abstraction, polymorphism, and encapsulation.

## Objectives
*   Implement OOP fundamentals such as classes, objects, and methods.
*   Apply inheritance to create a hierarchy of event types.
*   Use polymorphism to manage different community members attending events.
*   Work with arrays to store and manage events instead of `ArrayList`s.
*   Utilize encapsulation and access modifiers to protect data.

## Part 1: Class Design
- **1\. Create the Parent Class: `CommunityEvent`**
  - **Attributes:**
    *   `eventName` (public): Name of the event.    
    *   `eventDate` (protected): Date of the event.
    *   `ventDescription` (private): Description of the event.
  - **Methods:**
    *   Constructor: Initializes all attributes.
    *   `getEventDetails()` (public): Returns a formatted string with event details.
    *   `celebrateEvent()` (abstract): To be implemented in subclasses to describe how the event is celebrated.
- **2\. Create Child Classes that Inherit from `CommunityEvent`**
  - `CulturalFestival` Class
    *   Implements `celebrateEvent()`, describing how cultural festivals are celebrated (e.g., music, dance, food).
  - `LanguageWorkshop` Class
    *   Adds a new attribute `language` (public) to specify the language being taught.
    *   Implements `celebrateEvent()`, describing how the workshop promotes language diversity.
  - `VolunteerEvent` Class
    *   Implements `celebrateEvent()`, describing volunteer contributions to the community (e.g., assisting elders, cleaning public spaces).
    
## Part 2: Managing Events with Arrays
- **1\. `Team` Class (Aggregation Relationship)**
  - **Attributes:**
    *   `volunteerEvents[]` (private): Array to store `VolunteerEvent` objects.        
    *   `eventCount` (private): Tracks the number of events added.
  - **Methods:**
    *   Constructor: Initializes the array with a given size.
    *   `addVolunteerEvent(VolunteerEvent event)`: Adds an event if space is available.
    *   `listVolunteerEvents()`: Prints details of all stored volunteer events.
- **2\. `CulturalHub` Class (Composition Relationship)**
  - **Attributes:**
    *   `hubName` (public): Name of the cultural hub.
    *   `events[]` (private): Array to store `CommunityEvent` objects.
    *   `eventCount` (private): Tracks the number of events added.
  - **Methods:**
    *   Constructor: Initializes the event array.
    *   `addEvent(CommunityEvent event):` Adds an event if space is available.
    *   `listEvents():` Prints details of all stored events.
        
## Part 3: Implementing Polymorphism with `AbstractCommunityMember`
- **1\. Create the Abstract Class `AbstractCommunityMember`**
  - **Attributes:**
    *   `memberName` (public): Name of the community member.
    *   `memberRole` (public): Role in the community (e.g., Volunteer, Participant).
  - **Methods:**
    *   Constructor: Initializes attributes.
    *   `attendEvent()` (abstract): To be implemented by subclasses.
- **2\. Create Concrete Subclasses**
  - `Volunteer` Class
    *   Implements `attendEvent()`, describing how the volunteer helps at events.
  - `Participant` Class
    *   Implements `attendEvent()`, describing how the participant engages with events.

## Part 4: Testing the System in MyProgram

### Tasks to Complete in `main()`

1.  **Create and test event objects:** Instantiate `CulturalFestival`, `LanguageWorkshop`, and `VolunteerEvent` objects.
2.  **Call `celebrateEvent()` on different objects:** Demonstrate how each event type has a unique celebration message.
3.  **Create and test `Team`:**
    *   Instantiate a `Team` object.
    *   Add `VolunteerEvent` objects to the team.
    *   List all volunteer events.
4.  **Create and test `CulturalHub`:**
    *   Instantiate a `CulturalHub` object.
    *   Add different `CommunityEvent` objects.
    *   List all events in the hub.
5.  **Test Polymorphism:**
    *   Instantiate `Volunteer` and `Participant` objects.
    *   Call `attendEvent()` to show different behaviors for community members.

## Reflection Questions
1.  How does using inheritance simplify the structure of this system?
2.  What benefits does polymorphism provide in managing different types of community members?
3.  Why is encapsulation important in protecting event and member data?
4.  How does this project reflect real-world event organization and cultural diversity management?
    
## Submission:
*   Ensure all `TODO` sections in the starter code are completed.
*   Run and test the program to verify correct output.
*   Submit the final `.java` files with proper comments and indentation.
