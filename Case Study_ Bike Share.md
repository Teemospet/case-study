
> # Case Study: Bike-Share
> This case study is based on a fictional company and focuses on user behavior data. The objective is to make an analysis and develop a marketing strategy.
> 
> This case study contains 2 two parts, Final Report, which explains insights into the data and draws recommendations; and Data Wrangling Process, which documents in detail the steps taken to process the data.


> ## Final Report
>  ### Introduction
> In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime. Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.  Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day. 

> ### Goal
> Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships.
> 
> Therefore, we can analyze the Cyclistic historical bike trip data to identify trends in order to better understand how annual members and casual riders differ, what factors are driving annual members to choose our product, why casual riders would buy a membership and what can we do to convert casual riders into annual members.

> ### Tools
> Since the dataset of each month contains hundreds of thousands of records and consolidation into an entire year is a must,  [MySQL](https://www.mysql.com/)  and [Tableau Public](https://public.tableau.com/en-us/s/) is choosen for data wrangling and visualization.
> 
> The final dataset is a combination if 12 months records from 2021-Aug to 2022-Jul. Some additional columns are added to the dataset table for the purpose of easy handling in Tableau. Full steps of data wrangling are documented in second part of the report: Data Wrangling Process.

> ### Analysis
![222](https://public.tableau.com/views/BikeShare_16613854396780/TotalTripCount?:language=en-US&:display_count=n&:origin=viz_share_link)
>#### 

> 1. Average Time Spend
> 
> The pie chart from Figure - 1.1  shows that overall, members use the bikes 15% more often than casual users. However, as shown in Figures 1.2 and 1.3, casual users ride the bikes nearly twice as long as members. Members ride the bikes for nearly the same amount of time at all times of day. Casual users, on the other hand, try to avoid using the product for long periods of time during morning rush hours and prefer to use it during the day near noon from 10 AM to 3 PM.
> 
> 2. Usage of Time Periods
> 
> The heat map Figure - 2.1 shows the tendency of different user groups to use the product by date. Overall, the months of May through October are the most popular, with a significant drop in product usage during colder weather. Casual users mostly ride on weekends, whereas members are more evenly distributed, with a slight preference for riding on weekdays.
>
> The line graph Figure - 2.2 comfirms a significant drop in bicycle use during the winter months. Even so, bicycle use by members is still much higher than casual users in the winter. Casual users, on the other hand, have a larger variance gap and more dramatic fluctuations in bike use during the summer, implying a more specific use scenario than members.
>
> The bar chart for the monthly comparison Figure - 2.3 shows that casual users' bike usage drops sharply starting in October, while members are relatively less affected by [Chicago's weather or temperature](https://www.usclimatedata.com/climate/chicago/illinois/united-states/usil0225).
>
> The bar chart for the weekly comparison Figure - 2.4 reveals in more detail that recreational users only want to ride their bikes more on weekends, which is twice as much as weekday usage. However, member usage is fairly consistent throughout the week, with only a minor dip on weekends. 
>
> The bar chart for hourly comparison Figure - 2.5 illustrates that there are two bike usage peaks for members, one in the morning rush hour and one in the evening rush hour, with the evening peak being 40% higher than the morning peak. In the evening peak, there is a good usage rate for non-frequent users as well. Therefore, it can be inferred that the evening peak is a suitable usage scenario for both two categories of users.
>
> The pie chart in Figure 2.6 supplements the previous chart by showing that during the morning and evening peaks, member and casual users account for 40% and 31% of total usage, respectively.
>
> Based on the six charts above, it is possible to conclude that:
> - The product's demand will peak in the morning and evening rush hours.
> - Although weather has a greater impact on bicycles, members' off-season usage cannot be overlooked.
> - During weekends and holidays, casual users prefer to ride bikes more than members.
>
> 3. Bike Types Preference
> 
> Everyone's first choice is classic bikes. Whether it's a classic bike or an e-bike, members ride for shorter periods of time, either because they ride faster or for shorter distances. An e-bike can save members 1.5 minutes on average over a regular bike. No member would opt for a docked bike.
>
 > 4. Popular Stations
 > 
 > The map chart Figure 4.1 illustrates that customers prefer cycling near the coastline and in the downtown area. The most popular bike stations, which have some nice tourist attractions, are along the Red Line subway line north of Grant Park. Moreover, riders tend to choose downtown as their destination.
 > 
 > Figure 4.2 is a list of popular stations that emphersize casual users' preference. We can launch our marketing promotions from these stations.
 >  
 > 5. User Comparision Profile
 > 
 > We can now summarise the user's behaviour pattern and organise it into user comparision list based on the above analysis.
> | | Annual Members | Casual Users |
> |-|----------------------|--------------------|
> | | High demand for weekday morning/evening peak hour commute | Low demand for weekday  morning peak and medium demand for evening peak hour commute |
>| | Medium demand for weekend/holiday leisure | High demand for weekend/holiday leisure | 
>| | High preference in the summer and the fall | High preference only in the summer |
>| | Low travel time: more perposeful | High travel time: Less perposeful |
>| | Higt preference for downtown | Higt preference for downtown |
>

> ### Recommendations
> Let us divid the leisure users into two categories: 1) those who might have a high demand for bicycles but do not know it yet, and 2) those who clearly and explicitly know that their demand for bicycles is simply for occasional weekend/holiday recreation.
> 
> For the first categorie, we have a higher probability of converting them into members. The goal is to win their favour by putting a strong emphasis on needs. We can do the followings:
> - To find the casual users who use the bike more frequently and apply the RFM analysis, further dataset analysis regarding account data must be done.
> - Email alerts/app notifications to inform casual riders of the value of becoming a member.
> - Increase the number of advertisements for cycling in the summer, emphasizing the joy gained from being in the nature while cycling
> - Emphasize the time savings of commuting by bicycle in the morning and evening rush hours
> - Emphasize that cycling in the city center will be a better experience than driving
> - Emphasize that members can use the bike as many times as they want, emphasizing the use scenario
> - All of the above plans can also first be advertised on the most popular sites on a trial basis, and then gradually promoted according to the popularity of the site

> ## Data Wrangling Process

 1. Dataset
	 - Original dataset: [12 separate months](https://divvy-tripdata.s3.amazonaws.com/index.html)
	 - Finial dataset: [bike_2108_2207_v2](...)
	 - The data has been made available by Motivate International Inc. under this [license](https://ride.divvybikes.com/data-license-agreement)


