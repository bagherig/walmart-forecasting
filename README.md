**THE M5 COMPETITION**

The goal of this project is to provide **28-days** ahead point forecasts for **30490** various items sold by **Walmart**.

**The dataset**
===============

The M5 dataset, involves the
unit sales of various products sold in the USA, organized in the form of
**grouped time series**. More specifically, the dataset involves the
unit sales of **3,049 products**, classified in **3 product categories**
(Hobbies, Foods, and Household) and **7 product departments**, in which
the above-mentioned categories are disaggregated.  The products are sold
across **ten stores**, located in **three States** (CA, TX, and WI).

The historical data range from **2011-01-29** to **2016-06-19**, which consists of the following **three (3) files**:

**File 1: "*calendar.csv"* **

Contains information about the dates the products are sold.

-   *date*: The date in a "y-m-d" format.

-   *wm\_yr\_wk*: The id of the week the date belongs to.

-   *weekday*: The type of the day (Saturday, Sunday, ..., Friday).

-   *wday*: The id of the weekday, starting from Saturday.

-   *month*: The month of the date.

-   *year*: The year of the date.

-   *event\_name\_1*: If the date includes an event, the name of this
    event.

-   *event\_type\_1*: If the date includes an event, the type of this
    event.

-   *event\_name\_2*: If the date includes a second event, the name of
    this event.

-   *event\_type\_2*: If the date includes a second event, the type of
    this event.

-   *snap\_CA*, *snap\_TX*, and *snap\_WI*: A binary variable (0 or 1)
    indicating whether the stores of CA, TX or WI allow SNAP[^3]
    purchases on the examined date. 1 indicates that SNAP purchases are
    allowed.

**File 2: *"sell\_prices.csv"***

Contains information about the price of the products sold per store and
date.

-   *store\_id*: The id of the store where the product is sold.

-   *item\_id*: The id of the product.

-   *wm\_yr\_wk*: The id of the week.

-   *sell\_price*: The price of the product for the given week/store.
    The price is provided per week (average across seven days). If not
    available, this means that the product was not sold during the
    examined week. Note that although prices are constant at weekly
    basis, they may change through time (both training and test set).

**File 3: "*sales\_train.csv*" **

Contains the historical daily unit sales data per product and store.

-   *item\_id*: The id of the product.

-   *dept\_id*: The id of the department the product belongs to.

-   *cat\_id*: The id of the category the product belongs to.

-   *store\_id*: The id of the store where the product is sold.

-   *state\_id*: The State where the store is located.

-   *d\_1, d\_2, ..., d\_i, ... d\_1941*: The number of units sold at
    day *i*, starting from 2011-01-29.
