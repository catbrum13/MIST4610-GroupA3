**MIST4610-GroupA3**   
Catherine Brumbeloe - Group Leader  
Camryn Copeland- SQL Writer  
Joseph Halab - Data Wrangler  
Diya Mopur - Database Designer  
Sachit Juneja - Conceptual Modeler  

**Case Description**  
Live Music Circuit (LMC) organizes concerts around Athens, Georgia by managing venues, artists, events, staff, vendors, and equipment resources. They maintain records on all venues they work with and also track venue affiliations to document relationships between venues, past or present. Each concert, or event, takes place at a single venue on a specific date and time and includes one or more performing artists. LMC records these performances through artist bookings, which capture which artists appear at which events and in what order. Events may be free or ticketed, and LMC tracks all tickets associated with each event. Every event requires staffing, so LMC uses staff assignments to link a main coordinator and a backup coordinator to each event. Coordinators come from LMC’s pool of employees, whose basic information is stored in the system. LMC also manages resource items such as speakers and lighting, each belonging to a resource type that determines pricing for partner and non‑partner venues. Equipment can be scheduled for events through allocation records, which track when items are in use and ensure no item is double‑booked. In addition, LMC works with external vendors like food trucks or merchandise sellers. Vendor participation at events is tracked through vendor bookings, which record their involvement and logistics. Overall, the system connects venues, artists, staff, vendors, and equipment to support flexible event planning.

**Data Model**
Vendor and Event have a many-to-many relationship, creating a new entity Vendor Booking that has a one-to-many with Event and Vendor. One event has many vendor bookings and one vendor has many vendor bookings.  
Event and Ticket have a one-to-many relationship. One event sells many tickets and one ticket goes to one event.   
Event and Venue have a one-to-many relationship. One venue host many events and one event is at one venue.  
Event to Resource Item is a many-to-many, creating a new entity Resource Allocation that has a one-to-many with Event and Resource Item. One Event has many resource allocations and one resource item has many resource allocations.  
Resource Item and Resource Type have a one-to-many relationship. Each resource type can have many items, but each item can only have one type.  
Event and Artist has a many-to-many relationships, creating a new entity Artist Booking. One event host many artist and one artist plays many events. With the artist booking, one artist has many bookings and one event has many bookings.  
Event and Staff Assignment have a one-to-one relationship. One event has one staff assignment and one staff asignment has one event.  
Staff Assignment and Employee has two one-to-many relationships. One for a coordinator and one for a backup coordinator. Each staff assignment has one coordinator and one backup coordinator, and each employee can have many staff assignments.  
Venue and Venue Affiliation have two one-to-many relationships. One for Venue A and one for Venue B. A venue can have multiple venue affiliations, but each affiliation can only between one other venue.  



