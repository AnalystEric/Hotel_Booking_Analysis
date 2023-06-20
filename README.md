# <p align="center">Hotel Booking Analysis</p>
As Data Analyst Students at Codebasics.io, after learning various applications of Python, we will apply the concepts and functions we have learned to create our first data analysis project.

## Background of the project
An imaginary company called AtliQ Grands is a hotel chain that has operated in various cities in India for over 20 years. Their operations cover Delhi, Mumbai, Bangalore, and Hyderabad.

AltiQ Grands have four level hotels to let guests choose from AtliQ Seasons, AtliQ Exotica, AtliQ Bay, and AtliQ Palace. For example, AtliQ Palace is a luxury hotel, and AtliQ Seasons is a business hotel.
Furthermore, AtliQ Grand have different types of rooms: standard, elite, premium, and presidential. Customers can book the rooms on AtliQ's website or a third-party website.

**Five steps are included in the project.**
1. Understand Business Problem
2. Data Exploration
3. Data Cleaning
4. Data Transformation
5. Insight Generation

## Built with
Programming Language: Python

Libraries used: Pandas, Matplotlib

NoteBook: Jupyternote book

Dataset Source: Codebasics.io



## About the datasets

We have six CSV files for this project.

**Data Dictionary for the CSV file: fact_bookings.csv**    

    booking_id -> This column represents a unique identifier for each booking made.
    
    property_id -> This column represents a unique identifier for each property listed or available for booking. It is used to associate the booking with a specific property.
    
    booking_date -> This column indicates the date on which the booking was made. It represents the date when the reservation or booking transaction was initiated.
    
    check_in_date -> This column represents when the guest is scheduled to enter the property and begin their stay.
    
    checkout_date -> This column represents when the guest is expected to check out and end their stay at the property.
    
    no_guests -> This column indicates the number of guests included in the booking. It represents the total number of individuals staying at the property during the reservation period.
    
    room_category -> This column specifies the category or type of room or accommodation that was booked.
    
    booking_platform -> This column represents the platform or website through which the booking was made.
    
    ratings_given -> This column represents the ratings or feedback given by the guest after their stay. It typically reflects the satisfaction level or experience of the guest during their stay at the property.
    
    booking_status -> This column indicates the current status of the booking.
    
    revenue_generated -> This column represents the total revenue generated by the booking.
    
    revenue_realized -> This column indicates the actual payment realized or received by the property or booking platform.


- Total number of rows in data: 134590

- Total number of columns: 12


**Data Dictionary for the CSV file: dim_date.csv**

    date -> This column represents the date on which the booking was made.
    
    mmm yy -> This column represents the abbreviated month and year format.
    
    week no -> This column indicates the week number within a given year.
    
    day_type -> This column categorizes each day based on its type, specifically differentiating between weekdays and weekends.


- Total number of rows in data: 92

- Total number of columns: 4

**Data Dictionary for the CSV file: dim_hotel.csv**

    property_id -> This column represents a unique identifier for each property in the hotel analysis dataset.

    property_name -> This column stores the name or title of each hotel property.

    category -> This column indicates the type or classification of the hotel property.

    city -> This column stores the name of the city where the hotel property is located. 

- Total number of rows in data: 25

- Total number of columns: 4

**Data Dictionary for the CSV file: dim_room.csv**

    room_id -> This column represents a unique identifier for each room in the hotel analysis dataset.

    room_class -> This column indicates the class or type of the room.

- Total number of rows in data: 4

- Total number of columns: 2

**Data Dictionary for the CSV file: fact_aggregated_bookings.csv**

    property_id -> This column represents a unique identifier for each property in the hotel analysis dataset.

    check_in_date -> This column represents the date when guests checked into their rooms.

    room_category -> This column indicates the category or type of room booked by guests.

    successful_bookings -> This column represents the number of people or guests in each booking.

    capacity -> This column denotes the maximum room capacity in terms of the number of guests it can accommodate.

- Total number of rows in data: 9200

- Total number of columns: 5



**Data Dictionary for the CSV file: new_data_august.csv**

    property_id -> This column represents a unique identifier for each property in the hotel analysis dataset.

    property_name -> This column stores the name or title of each hotel property.

    category -> This column indicates the type or classification of the hotel property.

    city -> This column stores the name of the city where the hotel property is located. 

    room_category -> This column indicates the category or type of room booked by guests.

    room_class: This column indicates the class or type of the room.

    check_in_date: This column represents the date when guests checked into their rooms.

    mmm yy >This column represents the abbreviated month and year format.

    week no > This column indicates the week number within a given year.

    day_type > This column categorizes each day based on its type, specifically differentiating between weekdays and weekends.

    successful_bookings: This column represents the number of people or guests in each booking.

    capacity: This column denotes the maximum room capacity in terms of the number of guests it can accommodate.

    occ% This column represents the occupancy percentage for a specific combination of sucuessful_bookings and capacity.

- Total number of rows in data: 7

- Total number of columns: 13





## Understand
AtliQ is facing a significant challenge from its competitors, which means it is losing its revenue and market share. As a result, the CEO of AtliQ has decided to onboard data analytics using Python to make data-informed decisions so that it can increase its revenue.
