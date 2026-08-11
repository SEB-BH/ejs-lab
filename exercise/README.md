<h1>
  <span class="headline">EJS Lab</span>
  <span class="subhead">Exercise</span>
</h1>

# Requirements

## Page 1 — Home Page

1. Create a homepage.ejs file in your views folder. It should contain the following html inside:

The page should contain:

- A welcome heading (`<h1></h1>`)
- A short description of the website
- A link that says:

```
See Our Restaurants
```

2. Clicking the link should take the user to the restaurants page (`/resturaunts`). This link should not work yet because we haven't made the resturaunts page.

3. Now in your server.js write a route for this ejs page. Meaning if we get a request on `/` route then this ejs page should be displayed.

4. **CHECKPOINT**: Check that if you go to `http://localhost:3000` you see the homepage.ejs page

---

## Page 2 — Restaurants Page

1. Create a page called `all-resturaunts.ejs` in your `views` folder. For now just add an h1 like so `<h1>All Resturaunts</h1>`.

2. Now in your server.js write the route so when the user sends a request to `/resturaunts` they see the `all-resturaunts.ejs` page

3. Pass the resturaunts data to the ejs page as an object in the locales Object.

4. In the `all-resturaunts.ejs` page loop through all the resturaunts and display their name in an `<a></a>` tag

5. **CHECKPOINT**: make sure you see the resturaunts on the page as `<a></a>` tags.

6. Have it so the href for each a tag is linking to `/resturaunts/:id`. With id being THAT RESTURAUNTS id.

7. **CHECKPOINT**: Now when you click on the resturaunt link it should take you to something like this in the url: `http://localhost:3000/resturaunts/3`


## Page 3 — Restaurant Details

1. Create a page called `resturaunts-details.ejs` in your `views` folder. For now just add an h1 like so `<h1>Resturaunt details</h1>`.

2. Now in your server.js write the route so when the user sends a request to `/resturaunts/:id` they see the `resturaunts-details.ejs` page.

3. CHECKPOINT: In the `/resturaunts` route now when you click the link to a resutraunt it should show you the `resturaunts-details.ejs` page with the url looking like thos: `/resturaunts/3` for example

4. Now in the server.js for the route we just created (`/resturaunts/:id`) use the `.find()` method for the array to find the resturaunt that matches the id in the dynamic route parameter. **REMEMBER** the dynamic route parameter is in the `req.params`.
  - If in the route we had the url like so `/resturaunts/:id` then we can get the id at `req.params.id`
  - If in the route we had the url like so `resturaunts/:jameela` then we get the id at `req.params.jameela`

5. CHECKPOINT: `consoe.log()` what you get back from the `.find()` method to make sure that the resturaunt returns matches the id of the resutraunt in the url.

6. If your `.find()` method is correct and the right resturaunt is returned then pass that resturaunt to your .ejs view in the locales object.

7. Now in the `resturaunts-details.ejs` page display the resturaunt details: name, address, if its open, and phone number

## Navigation

Every page should include a navigation bar.

The navigation bar should contain links to:

* Home
* Restaurants

---

# Bonus Challenges

## Bonus Challenge 1

On the **Restaurants** page, display whether a restaurant is closed.

Example:

```
Al Baik

Haji's Traditional Cafe - Closed

Al Jabriya Turkish Restaurant
```

Hint:

The restaurant objects include an `isOpen` property.

---

## Bonus Challenge 2

On the **Restaurant Details** page, display the restaurant's menu.

Loop through the menu array and show:

* Item name
* Price
* Rating

Example:

```
Balaleet

Price: 1.8bd

Rating: 5
```

Repeat for every menu item.

---

## Bonus Challenge 3

create a `data.js` file and put the `resturaunts` array of objects in there. Export the resturaunts and import them in the `server.js`. 

- NOTE: Check that the website works the same now. All this does is take our data into a dedicated file as to not clutter up our `server.js`.

---

## Bonus Challenge 4


Make the navbar a partial if you haven't already.

---

## Bonus Challenge 5

Improve the appearance of your website by adding your own CSS.

Ideas:

* Style the navigation bar
* Add spacing between sections
* Create restaurant cards
* Use different fonts
* Display menu items inside cards

