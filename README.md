# Ford GoBike Service Data Exploration
## by Yasser Gharib
## Investigation Overview
Bike-sharing service like "Ford GoBike" is one of the rapidly growing transport services around the world, it has gained popularity in major cities across the globe. They allow people in metropolitan areas to rent bicycles for short trips usually within 30 minutes. Ford GoBike has collected a rich amount of data for this bicycle-sharing service from its electronic system in datasets. Each dataset includes information about individual rides made in a bike share system covering 
## Dataset Overview 
The project Dataset is provided by Ford GoBike sharing service at the greater San Francisco Bay area for ONE month (February 2019) with 183,412 bike trips, each one has 16 features available. some features for the Trip like: start_time, end_time, duration_sec, start_station_name, end_station_name, start_station_latitude, start_station_longitude, end_station_latitude,end_station_longitude, which bick in bike_id, but some for the bick like: bike_id, bike_share_for_all_trip and other for user (Riders) like: user gender (member_gender), age (member_birth_year), user_type.
The most interested features will include:
•	Trip features (start time/location, and duration) with new driven features: “Time period” (Morning, Afternoon, and Night) and “Week Day” (Mon, Tue, Wed, Thu, Fri, Sat, Sun), all from “start_time”
•	with Riders characteristics (gender, and user_type) with new driven feature “age” from “member_gender”

## Summary of Findings
The number of missing values rows in the dataset, is 8460 from 183412 rows, ie: 4.6% in 6 features (‘member_gender’, ‘member_birth_year’, ‘start_station_id’, ‘start_station_name’, ‘end_station_id’, ‘end_station_name’). We drop missing data row due to low % (4.61%), and found No duplicates exist.
### Univariate Exploration
•	There are outliers. Age from 18 to 55 takes 95% of the users. We remove users more than 60 years old.
•	The Ford bike users' median user age is around 33~34.
•	The most top 7 start stations with highest trips (over 2,500 trips) from 329 one,( ‘Market St at 10th St, San Francisco Caltrain Station 2 (Townsend St at 4th St)’, ‘Berry St at 4th St’, ‘Montgomery St BART Station (Market St at 2nd St)’, ‘Powell St BART Station (Market St at 4th St)’, ‘San Francisco Ferry Building (Harry Bridges Plaza)’, ‘San Francisco Caltrain (Townsend St at 4th St)’)
•	Where and Why most trips are taken?
•	After checking the top (most trips) 7 start and end stations in San Francisco are taken because this most stations were connect to public transportations such as CalTrain, Metro (Berry) stations, Ferry building and Market Street.
•	When the most trips are taken?
•	In these top 7 trips stations, we found:
•	During the day, there are more trips in the morning and afternoon than the night. It probably because of rush hours. Also, the number of trips in the afternoon is slightly less than the morning and bigger than night. may be bick riders go work in the morning and come back home in afternoon, and might not be back in the night.
•	It makes sense that there are more trips during the weekdays and less trips during the weekends because of working schedule.
•	Most durations of trips fall into 600 seconds (10.0 minutes).
### Relationships in bivariate exploration.
In the top 7 stations, look into the attributes' times and users:
1.Time:
•	After separating into 7 stations, there are more trips in the morning and afternoon than the night. the number of trips in the afternoon is slightly less than the morning and bigger than night.
•	It makes sense that there are more trips during the weekdays and less trips during the weekends because of working schedule.
2.User:
•	Age: most of age population falls between 30 and 40 years old. It might imply there are full time employees and commuters.
•	Gender: the number of trips in males is way more than the number in females. It needs to be investigated more.
•	Subscribe: the number of trips in subscribers is more than the number in customers because of pricing and population.
### Multivariate Exploration
After separating customers from subscribers, there are some very interesting findings in these 3 time categorical variables.
•	Time of Day: there are more trips in the morning or afternoon no matter in customers or subscribers.
•	Weekdays: it implies customers probably includes tourists because most trips happen in the weekend. On the other hand, subscribers imply commuters because most trips happen in the weekdays.
Features strengthen each other in terms of looking at locations and times
The Relation between user types (customers, and subscribers), displays more information from location and time. Customers might be tourists who like to use a bike during the weekend. Also, the number of trips increases in the tourist attractions like Ferry building and Embarcadero (close to piers). On the other hand, subscribers might be commuters. The trips in subscribers increase during the weekdays and afternoon.

