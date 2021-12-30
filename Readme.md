**Application**** of ****Data**** Science ****for**** Developing ****a**** Hotel ****Selection**** System**

# Motivation:

In today&#39;s data-driven world, several e-commerce businesses have emerged that use data to helpcustomers find their desired items which match to their personal preferences. These businessesprovide customers with an online selection system in which they can filter items based uponparticular information and features. In fact, selection systems collect classified information aboutagroupofproductsorservicesandfilterthembasedonthespecificneedsofindividualusers.Forexample, online travel agencies, such as Expedia and Priceline, help travelers with findingavailable hotels/properties that meet their expectations regarding price, star rating, number ofrooms,amenities, location, etc.

# IntroductiontotheProject:

Inthisproject,youaregoingtohelpwithbuildinga&quot;HotelSelectionSystem&quot;,usingtwodatasets,i.e., Property\_details and Order\_details. All the columns in these two datasets are explained indetailas below:

## Property\_details:

_propertyid_: The ID of the property._propertyname_: The name of the property._address_:Theaddressoftheproperty.

_city_: The city where the property is located._country_:Thecountrywherethepropertyislocated._zipcode_:Thezipcodeof theproperty.

_propertytype_: The type of the property, i.e., Hotels, Inns, Motels, etc. (8 types in total)._starrating_: The star rating of the property, from 1 to 5 (e.g., 4 indicates a 4-star property)._latitude_:Thelatitudeof theproperty.

_longitude_:Thelongitudeoftheproperty.

_url_:Thewebsitelinktobooktheproperty(notnecessarilytheofficialwebsite).

## Order\_details:

_id_:Theid of the order.

_PropertyCode_:TheID oftheproperty.

_dtcollected_:Thedateofcollectingtheinformationoftheproperty.

_reservationdate_:Thedatethattheorderwasreceived.

_los_:Thelengthofstay(i.e., thenumberofnightsthat agueststaysintheproperty).

_guests_:Numberofguests whostayintheproperty.

_roomtype_:Theroomtypethat isbooked.

_onsiteprice_:Thepriceacustomerwouldpayfortheorder.

_ratedescription_:Thebookedroomdescription,whichmayincluderoomsize,numberofbedroomsandbeds, etc.

_ratetype_:Bookinginformation,includingcancellationpolicy,possiblepayinhoteloption,andextralow-pricereminding.

_sourceurl_:Thewebsitelinktobooktheproperty(notnecessarilytheofficialwebsite).

_roomamenities_:Theamenitiesavailableofthebookedroom.

_maxoccupancy_:Themaximumnumberofguestsallowedtostayinthebookedroom.

_ispromo_: Whether promotion is used when the order is placed (Y means in promotion, N meansnotin promotion).

_closed_: Whether the hotel is closed when the order is placed (Y means close, N means not close)._discount_: The monetary value of the discount that an order received (already been deducted fromthe&quot;_onsiteprice_&quot;).

_promoname_: The name of the promotion that the order participated in._proxyused_: The proxy used to retrieve the order data._mealinclusiontype_:Thetypeof meal includedin theorder.

_hotelblock_:Whetherthehotelwasfullybooked(SoldOutmeansnoroomsareavailableforanorder,Blank means rooms are availableforan order).

_input\_dtcollected_:Thedateinputtingthecollecteddataofthehotel.

You are required to use the Pandas and Numpy packages in order to read the above csv files andanalyze their data.

**QUESTIONS**

1. Part (a): How many properties are there in the region with the zip code of 84100?

Part (b): What is the mean, standard deviation, median, min, and max of &quot;starratings&quot; for all properties in the region with the zip code of 84100?

1. Part (a): Create a new column called &quot;weekday&quot;, which is the day of the &quot;reservation date&quot; in one week (for example, if the reservation date is 2021/10/22, the corresponding value in the new column &quot;weekday&quot; should be &quot;Friday&quot;).

Part (b): Which &quot;weekday&quot; does receive the most reservation?

1. Part (a): In &quot;roomamenities&quot;, what are the top 10 common room amenities? What about the 10 least common room amenities? ( for example, Air conditioning is one amenity)

Part (b): What percentage does each type of room amenities occupy of the total number of reservations for all properties?（do not use the total number of amenities as denominator）

1. Part (a): For each property, there are some abnormal values of 0 in the &quot;onsiteprice&quot;. To better organize the data, you would like to create a new column &quot;replaced onsiteprice&quot; in the dataset by retaining the original non-zero &quot;onsiteprice&quot; of one specific property and replacing the zero value with its median of non-zero &quot;onsiteprice&quot;.

Part (b): For each property, calculate the maximum and minimum value of &quot;replaced onsiteprice&quot;, and store these two into corresponding two columns named &quot;Maximum&quot; and &quot;Minimum&quot;. Then create a column named &quot;Normalized Maximum&quot; to store the normalized form of the &quot;Maximum&quot; column. You can use the formula below for the normalization (do not round the result). Store the &quot;hotelcode&quot;, &quot;Maximum&quot;, &quot;Minimum&quot;, &quot;Normalized Maximum&quot; to &quot;Mx\_Min Price.csv&quot;.

$ X\_{norm} = \frac{X-X\_{min}}{X\_\max-X\_{min}}$

1. Part (a): A family of three is planning a trip. How many available hotels do offer a room with the &quot;maxoccupancy&quot; of 3 or more? Available hotel are those whose &quot;propertype&quot; are &quot;Hotels&quot;, &quot;close&quot; are &quot;N&quot;, and &quot;hotelblock&quot; are not &quot;sold out&quot; .

Part (b): If this family does not want to pay a room for a &quot;replaced onsiteprice&quot; higher than 150 per night, how many hotels are still available? Use the maximum of &quot;replaced onsiteprice&quot; to compare with 150 due to price fluctuation.

1. Part (a): For each country, find the most expensive property by using &quot;replaced onsiteprice&quot;. Provide id, name, city, country, zip code, address, and average &quot;replaced onsiteprice&quot; of these properties.

Part (b): For each country, find the cheapest property by using &quot;replaced onsiteprice&quot;. Provide id, name, city, country, zip code, address, and average &quot;replaced onsiteprice&quot; of these properties.

Hint: Each country has numbers of hotels, and each hotel has numbers of prices due to price fluctuation. You need to find the average &quot;replaced onsiteprice&quot; for each hotel first, and sort out the cheapest and the most expensive hotels then.

## Business Questions

1. **How do prices compare with max occupancy in switzerland ?**

From analysis on the data provided, the following questions were formulated. The first question that was tackled was if there was a relatioship that existed between max occupancy and the onsite price. The case of switzerland was  selected to be the focus of the question. From the boxplot of max occupancy against replaced onsite price, the replaced onsite price,increased, generally as the maximum number of occupancy increased. The maximum occupancy of one had a lot of outliers and also was  higher than two and three maximum occupancy. This is because of the large variaety of property types that offered one maximum occupacy. The type of properties that offer two or more maximum occupancy, reduce significantly, and those that do, have the same characteristics and therefore, charge the same. A case study was selcetd because, prices change significantly from country to country, and each country has its unique characteristics in terms of price and property types.

1. **Which is are the most expensive cities in Greece ?**

Greece is known is for its rich historical cultural heritage, it therefore makes sense to identify which areas are the most expensive; for customers to plan ahead on the charges they expect to incur or select other areas. In determining the most expensive cities in Greece, the cheapest cities were also identified, therefore the customer was given more option. For one intending to start a business, one can determine how to set the appropriate prices if they are start the business there. The most expensive cities were Mykonos, Naxos Island, Kamares, Kylini, Tsilivi and Corfu Town. The error bars on the plot showed that prices  are not fixed, they have a range, a huge one, therefore, the properties charge prices on their own merit, it is a free market.

1. **Which day has the highest discount generally for the whole dataset and that of Italy ?**

The relationship between discounts and the day of the week was explored. Based on the day of the week, hotels could be offering some kind of discount. There were two approaches in this instance. The whole dataset, that is all countries and the second one was that of Italy. Sundays in both instances offered the largest discount and on Thursday. Sundays because, probably people are travelling to work conferences that take place when the week starts and on Thursday, it is end of week and people are making reservations for weekend entertaininment, that begins at end of Friday&#39;s working day. The treend above howeveris not the case for Italy. The discounts do not differ much in the global dataset, but one can note that for Italy, the discounts for different days have significant differences.

1. **Compare the starratings and discounts in Romania and France?**

Discounts vs Star rating: From the plot above comparing French and Romanian hotels, there seems to exist a relation between the amount of discount offered by a hotel and how customers rate the hotel. First, French hotels offer higher discounts, than Romanian Hotels. In both cases, hotels offering higher discounts  are rated higher than hotels that offer lower discounts.

1. **Compare discounts in United Kindom and Germany ?**

United Kingdom vs Germany

Four Star rated hotels and two star rated hotels in the United Kingdom are more expensive than those in Germany. Three star rated hotels in Germany are more expensive than in the United Kingdom. The information will help one determine the prices of the hotels if they were to set in Germany or the United Kingdom, or customers to plan ahead, if they are travelling through the European Union.

## Analysis 2 Business Questions

##

1. **Which 10 cities are the most frequented cities in the world ?**

The approach taken for this assignment was to look at the best performing cities in the world, and try to benchmark with them to determine which aspects of the recorded data, made them to be reserved in the world. London and Paris had the most orders to reserve hotels when compared to the other hotels. It is important to note that there is a huge gap between the reservations made in the first two cities, when compared to the rest of the cities.

1. **How do prices compare with max occupancy in the 100 most frequented cities ?**

The second step was to look into the price differences of hotels in the top 10 cities that were set aside in the first step. Since prices are also impacted by the max occupancy of the property. From the plot, note that London offers property with occupancy that goes beyond 6. However, the prices for this property, the prices are also very high. For the rest of property with max occupancy less than 6, the prices are generally the same, except for Edinburg amd Barcelona, the two cities are cheaper.

1. **How do discounts compare with max occupancy in the 100 most frequented cities ?**

The next comparison between the 10 cities was that of discounts against max occupancy rooms. London seems to offer the lowest discounts on the property with large max occupancy such as that of 6. London when compared to the rest of the cities generally gives the lowest discounts on the various max occupancy of the property. Manchester and Edinburg offer the highest discounts on room with maximum occupancy from 1 to 3. It is also important to note that hotels in Edinburg, Munich and Berlin, offer  a range of discounts from very discounts to very large discounts.

1. **What is the general distribution of star rating of this cities ?**

London, Paris and Edinburg appear to have ratings that range from 2 to offer, with London and Edinburg having the highest number of hotels in all the cities with the various ratings. This however, might not reflect the actual case because London  has the highest number of hotels in the dataset being considered. So far we can conclude that Edinburg is the best city to make a reservation and or set up a hospitality business.

1. **Which hotels are most frequented in the 10 cities ?**

Note that the hotels with reservations that are over 100 are mostly from the United Kingdom. Out of the top ten hotels only two are from outside the United Kingdomm, one from Spain and the other from France.

##