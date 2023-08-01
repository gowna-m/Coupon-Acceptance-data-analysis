# Coupon Acceptance Data Analysis

## “Will a customer accept the coupon?”

### Data Description
The data consists of different driving scenarios defined by user features and contextual features including the destination, current time, weather, passenger, gender, Marital Status etc., and the target variable being a binary defining the customers if they accepted or rejected the coupons. 
Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as `Y = 1` and answers ‘no, I do not want the coupon’ are labeled as `Y = 0`. 
There are five different types of coupons named _less expensive restaurants (under $20)_, _coffee houses_, _carry out & take away_, _bar_, _expensive restaurants ($20 - $50)_.

As part of the **Data understanding and Data preparation**, checked for null values along each feature and dropped the below attributes.
1.`Car` -  The car feature had 99% NaN values.<br />
2.`toCoupon_GEQ5min` - This feature describes the driving distance to the restaurant/bar for using the coupon is greater than 15 minutes and it had                          just one value for all the datapoints.<br />
3.`direction_opp` - This feature tells us whether the restaurant/bar is in the same direction as your current destination.It was a complementary feature of another feature named `direction_opp`.<br />

Apart from these features, there were a few categorical features that had a small percentage (~ 1%) of missing values - `Bar`,`CoffeeHouse` `CarryAway`,`RestaurantLessThan20`,`Restaurant20To50`. The NaN values here was replaced with the mode of the corresponding feature.

Next is the **Data Analysis**, the acceptance rate calculated for the total observations is **57%**. The coupon feature was visualized on a multiple stack bar plot and the temperature feature was plotted on a histogram.
Explored how the `bar` coupon made an impact on the acceptance rate,<br />
1. **41%** bar coupons were accepted.<br />
2. The acceptance rate of those who went to a bar 3 or fewer times a month is (**37%**) and those who went more is (**77%**)
3. The acceptance rate of drivers who go to a bar more than once a month and are over the age of 25 is (**70%**) and those who never went or went to the bar lesser than once and below the age of 25 is (**34%**).
4. The acceptance rate of drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry is **71%** and those those who never went or went to the bar lesser than once and had a passanger as a kid and had occupation as farming, fishing, or forestry is **30%**.
5. The acceptance rate of drivers who went to the bar more than once a month and had passanger that were not a kid(s) and age < 30 and go to cheap restaurants more than 4 times a month and income < 50K is **57%** and drivers who went to the bar less than once a month or never went to the bar and had passanger that were a kid(s) and age > 30 and go to cheap restaurants less than 4 times a month and income > 50K is **30%**.











