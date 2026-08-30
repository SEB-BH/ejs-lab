<h1>
  <span class="headline">EJS Lab</span>
  <span class="subhead">Setup</span>
</h1>


# Setup

Use our [starter document](https://docs.google.com/document/d/1Skjcc3gQG1lPhW5qCw8wfAzoI5W1oYvjGt4KqD_fUr4/edit?usp=sharing) to set up your Express application.


---

# Data

1. Paste the following array inside your server.js file right below the imports at the top:

```js
// DATABASE
const resturaunts = [
  {
    id: 1,
    name: 'Al Baik',
    isOpen: true,
    address: 'City Centre Road 4650, Manama',
    phone: '55509876',
    menu: [
      {
        name: 'Chicken Filtet Sandwich',
        price: .750,
        rating: 5
      },
      {
        name: 'Fish Filet Sandwich',
        price: .900,
        rating: 5
      },
      {
        name: 'Chicken Nuggets',
        price: 1.8,
        rating: 4.9
      },
        ]
  },
  {
    id: 2,
    name: "Haji's Traditional Cafe",
    isOpen: false,
    address: '150 شارع الحكومة, Manama',
    phone: '06892543',
    menu: [
      {
        name: 'Chicken Machboos',
        price: 2.2,
        rating: 4.5,
      },
            {
        name: 'Balaleet',
        price: 1.8,
        rating: 5,
      },
      {
        name: 'Cheese Omlette',
        price: .7,
        rating: 5,
      },
          ]
  },
  {
    id: 3,
    name: 'Al Jabriya Turkish Restaurant',
    isOpen: true,
    address: 'Rd No 2643, Busaiteen',
    phone: '17330108',
    menu: [
      {
        name: 'Roosy Sarookh',
        price: 1.8,
        rating: 5,
      },
      {
        name: 'Cheese Pizza',
        price: 2.5,
        rating: 3.5,
      },
      {
        name: 'French Fries',
        price: 1.2,
        rating: 4.3,
      },
        ]
  }
];
```




2.  Explore the data. What is the data structure. What data do we have on EACH resturaunt?



---