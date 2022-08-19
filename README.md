# Citi Bike Analysis using Tableau

Link to Tableau Public Link to Project: https://public.tableau.com/app/profile/grace.olson/viz/18-CitiBike-TableauChallenge/CitiBikeComparisonStory

In my analysis of the Citi Bike data, I use two datasets to determine if there is a significant difference in ride data between the winter and summer months. I used the January 2022 csv as my representation/proxy for the winter months and the June 2022 csv as my representaion/proxy for the summer months. 

You can find the Citi Bike datasets from June 2013 - present at this link: https://ride.citibikenyc.com/system-data

## Analysis #1: Average Distance of a Citi Bike Trip in January vs. June
* To analyze the average distance of a Citi Bike trip, I created three calculated fields for each csv: 
    1. An Origin Point using MAKEPOINT and feeding in Start_Lng and Start_Lat
    2. A Destination Point using MAKEPOINT and feeding in End_Lng and End_Lat
    3. A Distance calculation using DISTANCE and feeding in the created origin and destination points. 
* I also created a 'Weekends' set that would allow me to visualize the average distance travelled on a weekend day vs. a weekday.

* Using the distance calculated field, I created three visualizations comparing the average distance travelled in January vs. June:
    1. Average Trip Distance 
    2. Average Trip Distance by Member Type and Ride Type
    3. Average Trip Distance on a Weekend Day vs. a Weekday

* Three unexpected phenomena came out of my analysis of the average distance travelled:
    1. Despite the difference in climate, the average distance of a Citi Bike trip in January is only about 0.2 miles shorter than the average trip distance in June. Since the weather is typically significantly worse in January than it is in June in NYC, I would have excpected the average distance travelled in January to be much shorter.
    2. While the distribition of ride type remains relatively consistent regardless of time of year, the average trip appears longer for casual riders than for members in both months. This is surprising considering casual riders are more likely to get lost or travel to the wrong destination.
    3. The average distance travelled does not vary between weekday trips and weekend trips in either the winter (January) or the summer (June). This was a surprising find since weekday trips are typically more consistent, while weekend trips are typically more variable by tourists. Additionally, the number of casual riders vs. members on the a weekend day vs. a weekday appears to be very similar, which is also surprising considering the number of tourists (and likely casual riders) that arrive on the weekend. 

## Analysis #2: Popular Citi Bike Start Stations in January vs. June
* No calculated fields or groups/sets were needed to analyze popular start stations for Citi Bike trips in January vs. June as I added Member and Ride type detail to each chart.

* It was not surprising to find the number of Citi Bike rides was much higher in June than in January, presumably because of the nicer weather in June. However, two unexpected phenomena came out of my analysis of popular start stations for Citi Bike trips:
    1. Among casual riders, I found there is quite a bit of variability between the top 10 popular start stations between January and June. This find was not surprising as casual riders are likely not consistently riding and thus do not have a "home" station. It is interesting, however, that casual riders in January are relatively split between picking an electric bike vs. a classic bike at each station while casual riders in June much prefer classic bikes, regardless of start station. Perhaps this is because casual riders are more comfortable with electric bikes in the winter?
    2. For members, the most popular station appears to be W 21 St. &  6 Ave. for both January and June. The fact that members prefer the same station regardless of time of year is not surprising as most members likely have a "home" station. However, compared to casual riders, members much prefer to ride a classic bike, regardless of month and start station. As I do not live in NYC, the preference for a classic bike was interesting as we see a lot of electric bikes/scooters in Atlanta. Perhaps either a classic bike is easier to handle in the city or members are more focused on the exercise element of the ride than casual riders. 

* Note: while the raw data csvs show significantly more rows (rides) than what is shown in my popular stations dashboard / auto-generated count of csv rows, I have to assume this is because of the speed of my computer/what my computer can handle. The counts, however, preserved the relationship between the two months and are therefore representative of the entire dataset for both months.

## Map Analysis
* Four maps were created to visualize start and end stations in January and June. I used color and size detail as a visual inidator of station popularity and included the station name in the detail. 

* Two interesting findings from the maps analysis include:
    1. The popularity of start stations in June appear more distributed than in January based on the separation and count of dark blue circles and the size of markers on the June Start Stations map, while the popularity of end stations appear relatively evenly distributed between January and June based on the very similar separation of dark orange circles and size of markers on the two End Station maps. 
    2. 12 W Ave & W 40th Street becomes a very popular start and end station in June compared to January. There are a few other cases similar to this, and it would be interesting to do some research to find what is near these stations that makes their popularity increase in the summer months. 

* Note: while the instructions ask for zip code data to be overlaid on each map, zip codes were not included in the raw datasets and they are not a built-in layer in Tableau, thus this step was omitted. 

