# Restaurants_Catalog
This project will develop an application that provides a list of restaurants with a variety of Menus as well as provide a user registration and authentication system. Registered users will have the ability to post, edit and delete their items.

## URL Extentions 
- Display a list of all restaurants in the Database:
`/` or `/restaurant`
- Connect to login page with Google Oath:
`/login`
- Logout from the website and disconnect the user Google info:  
`/gdisconnect`
- Display a specific (chosen from the list or by intering restaurant_id) restaurant with its menu:
`/restaurant/<int:restaurant_id>/menu/JSON`
- Create new restaurant to add to database of the website:
`/restaurant/new/`
- Edit an existing restaurant to change its name:
`/restaurant/<int:restaurant_id>/edit/`
- Delete a restaurant from the website database:
`/restaurant/<int:restaurant_id>/delete/`
- Display restaurant list as JSON file which can be used as an input for other uses: 
`/restaurant/JSON`

- Display the content of a spesific resturant menu:
`/restaurant/<int:restaurant_id>/`
`/restaurant/<int:restaurant_id>/menu/`
- Create new menu item to add the the chosen restaurant:
`/restaurant/<int:restaurant_id>/menu/new/`
- Edit a menu item (name, Description, price, and course type):
`/restaurant/<int:restaurant_id>/menu/<int:menu_id>/edit`
- Delete a menu item from website database:
`/restaurant/<int:restaurant_id>/menu/<int:menu_id>/delete`
- Display menu as JSON file:
`/restaurant/<int:restaurant_id>/menu/JSON`
`/restaurant/<int:restaurant_id>/menu/<int:menu_id>/JSON`

## License
`Restaurants_Catalog` is a released under the [MIT License](https://opensource.org/licenses/MIT)
