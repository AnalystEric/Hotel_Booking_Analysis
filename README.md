# <p align="center">Hotel Booking Analysis</p>

## Built with
Cloud: Microsoft Azure Blob storage

Programming Language: Python

Libraries used:
- Pandas - for data manipulation (data exploration and data cleaning) and analysis 
- Matplotlib.pyplot - for creating visualisations, and pyplot provides a simplified interface for creating charts and plots
- Numpy - for numerical computing

NoteBook: Jupyternote book

## Project Overview
Using Python to make data-informed decisions, this project aims to help a hotel chain increase its revenue by presenting key findings on hotel performance metrics such as occupancy rates, revenue trends, and customer satisfaction scores. This approach enables data-driven decision-making.

**Five steps are included in the project.**
1. Understand Business Problems
2. Data Exploration
3. Data Cleaning
4. Data Transformation
5. Insight Generation


## About the datasets
**Developed cloud backend utilising Azure Blob storage.**

![Screenshot 2023-07-11 at 20 35 52](https://github.com/AnalystEric/Hotel_Booking_Analysis/assets/127030648/910a21dd-ec98-48ee-9297-c49224798f1b)


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

## Insight Generation

**1. What is the average occupancy rate in each of the room categories?**

    room_class      occ_pct
    Presidential    59.28
    Premium         58.03
    Elite           58.01
    Standard        57.89
    Name: occ_pct, dtype: float64


The standard, elite, premium, and presidential rooms have occupancy rates of 59.28%, 58.03%, 58.01%, and 57.89%, respectively.
The presidential room has the highest occupancy rate, while the standard room has the lowest occupancy rate.
However, there is not a significant difference in the occupancy rates among these four types of rooms; they all have around 58% of occupancy rate.

**2. What is the average occupancy rate per city?**

    city         occ_pct
    Delhi        61.51
    Hyderabad    58.12
    Mumbai       57.91
    Bangalore    56.33

The result displays that the occupancy rates of Delhi, Hyderabad, Mumbai, and Bangalore are 61.51%, 58.12%, 57.91%, and 56.33%, respectively.
Delhi has the highest occupancy rate, while Bangalore has the lowest occupancy rate.

**3. What are the average occupancy rates for weekdays and weekends, and which one is better, weekdays or weekends?**

    day_type    occ_pct
    weekend     72.34
    weekeday    50.88
    Name: occ_pct, dtype: float64

The average occupancy rate on weekends is significantly greater than on weekdays. The average occupancy rate at weekends and weekdays is 72.34% and 50.88%, respectively.

    To increase the occupancy rate on weekdays and generate more revenue for AtliQ, I have come up with two strategies:**

    Targeted Marketing: Develop a targeted marketing campaign specifically tailored to attract weekday guests, such as highly-promoted weekday offers, special discounts, or discounted rates to incentivize them to choose weekdays for their stay.

    Loyalty Program: Develop a loyalty program that rewards guests for staying on weekdays. Offer exclusive benefits or discounts for repeat weekday and weekend guests to incentivize their loyalty and increase weekday occupancy.


**4. What were the average occupancy rates in different cities in June?**

    city         occ_pct
    Delhi        62.47
    Hyderabad    58.46
    Mumbai       58.38
    Bangalore    56.44
    Name: occ_pct, dtype: float64

The average occupancy rates of Delhi, Hyderabad, Mumbai, and Bangalore in June are 62.47%, 58.46%, 58.38%, and 56.44% respectively.

**5. We got new data for the month of August. Append that to existing data.**

**6. What is the total revenue_realised per city?**

    city         revenue_realised
    Mumbai       668569251
    Bangalore    420383550
    Hyderabad    325179310
    Delhi        294404488

The result indicates the revenue realization in each city, with Mumbai having the highest revenue, followed by Bangalore, Hyderabad, and Delhi.
Mumbai may have a larger market size or higher demand for the services offered by AtliQ, resulting in higher revenue realization compared to other cities.

    To increase the revenue realisation in Bangalore, Hyderabad, and Delhi for AtliQ. I have come up with one strategy:

    Partnerships and Collaborations: Build partnerships with local businesses, travel agencies, or event organisers to tap into their networks and attract more 
    customers. Collaborations can result in mutually beneficial marketing opportunities and increase revenue.

**7. What is the month-by-month revenue?**

    mmm yy    revenue_realized
    Jul 22    243180932
    May 22    234353183
    Jun 22    229637640
    Name: revenue_realized, dtype: int64

The highest revenue was recorded in July 2022 with 243,180,932, followed by May 2022 with 234,353,183, and June 2022 with 229,637,640.

**8. What is the total revenue realized per hotel type?**

    property_name    revenue_realized
    Atliq Exotica    133619226
    Atliq Palace     125553143
    Atliq City       118290783
    Atliq Blu        108108129
    Atliq Bay        107516312
    Atliq Grands      87245939
    Atliq Seasons     26838223
    Name: revenue_realized, dtype: int64

Atliq Exotica emerges as the top-performing hotel with the highest revenue of 133,619,226. It is closely followed by Atliq Palace and Atliq City, which generated revenues of 125,553,143 and 118,290,783, respectively. Atliq Grands secured revenue of 87,245,939, while Atliq Seasons recorded comparatively lower revenue of 26,838,223.

<img width="1071" alt="Screenshot 2023-06-23 at 16 57 02" src="https://github.com/AnalystEric/Hotel_Booking_Analysis/assets/127030648/12ea091a-8f12-4409-a737-7e2b31ed583c">

**9. Create a bar chart to show the average rating per city.**

    city         ratings_given
    Delhi        3.79
    Mumbai       3.66
    Hyderabad    3.65
    Bangalore    3.41
    Name: ratings_given, dtype: float64

The given result displays the guests' ratings for four cities: Delhi (3.79), Mumbai (3.66), Hyderabad (3.65), and Bangalore (3.41).
Delhi has the highest rating, while Bangalore has the lowest rating among the four cities.

<img width="898" alt="Screenshot 2023-06-23 at 16 57 35" src="https://github.com/AnalystEric/Hotel_Booking_Analysis/assets/127030648/509abce6-2dd8-4ee6-8dba-f7ea2ce4b821">

**10. Create a pie chart to show the total revenue realized per booking platform.**

    booking_platform   percentage
    direct offline     5.0
    direct online     10.0
    journey            6.0
    logtrip           11.0
    makeyourtrip      20.0
    others            41.0
    tripster           7.0
    Name: revenue_realized, dtype: float64
<img width="837" alt="Screenshot 2023-06-23 at 16 31 39" src="https://github.com/AnalystEric/Hotel_Booking_Analysis/assets/127030648/485c994d-eb5a-4bbc-b042-c134ad1ed40e">

"Others" contributed the highest percentage, accounting for 41% of the total revenue.

"Makeyourtrip" followed with a contributition of 20%.

"Logtrip" and "diret online" had moderate contributions of 11% and 10%, respectively.

"Direct online", "joureny" and "direct offline", had relatively lower percentages ranging from 5% to 7%.




