<img src="Restaurant_Icon.png" width="100">

# Restaurants_Catalog
This project will develop an application that provides a list of restaurants with a variety of Menus as well as provide a user registration and authentication system. Registered users will have the ability to post, edit and delete their items.

## Installation and Run
In order to install and run the project please follow the following steps:
1. Download or clone the project at [here](https://github.com/Nshmais/Restaurants_Catalog) or run this in the command line:
   ```
      $ sudo apt-get install git
      $ git clone https://github.com/Nshmais/Restaurants_Catalog
      $ cd Restaurant_catalog
      $ python Start.py 
   ```
2. The project will run on the appropriate port (for this project it's localhost:5000) or check the command line.
3. To terminate the project from local host in commandline type  **^C** which is **Ctrl+C**.
4. To terminate the VM type  **^D** which is **Ctrl+D**.

## Required Libraries and packages
The project code requires the following software packages:
- SQLAlchemy
- Python 2.7
- Flask
- The following Python packages: oauth2client /requests /httplib2

## Database Setup
The database can be setup by running `database_setup.py`file
```
   $ python database_setup.py
```

## Database Populate
The database can be populated in three ways:
1. Just insert every resturan and it's menu at a time from the web pages of creating new restaurant.
2. Edit `lotsofmenus.py` file using sublime or your favorite text editor program:
   Edit the lines to reflect your Entries, example name of the restaurant (name=Le Bernardin), and your user_id for example (user_id=8)
   ```
   restaurant1 = Restaurant(user_id=8, name="Le Bernardin")
   session.add(restaurant1)
   session.commit()
   ```
   also add menu name, description, price, and course type:  
   ```
   menuItem1 = MenuItem(user_id=8, name="", description="", price="", course="", restaurant=restaurant1)
   session.add(menuItem1)
   session.commit()
   ```
   just like that you can add (menuItem2) and (menuItem3)and so on.
3. This is the most complicated one, you can download [DB Browser for SQLite](http://sqlitebrowser.org/), DB Browser for SQLite 3.9.1 for [Windows](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/v3.9.1) it's also avilable for other OSes, and edit the `restaurantmenuwithusers.db` file directly using the DB Browser. 
## URL Extentions 
This website has many expentions that display assigned pages if added to the end of the **http://localhost:5000** URL:
1. Display a list of all restaurants in the Database:
`/` or `/restaurant`
2. Connect to login page with Google Oath:
`/login`
3. Logout from the website and disconnect the user Google info:  
`/gdisconnect`
4. Display a specific (chosen from the list or by intering restaurant_id) restaurant with its menu:
`/restaurant/<int:restaurant_id>/menu/JSON`
5. Create new restaurant to add to database of the website:
`/restaurant/new/`
6. Edit an existing restaurant to change its name:
`/restaurant/<int:restaurant_id>/edit/`
7. Delete a restaurant from the website database:
`/restaurant/<int:restaurant_id>/delete/`
8. Display restaurant list as JSON file which can be used as an input for other uses: 
`/restaurant/JSON`

9. Display the content of a spesific resturant menu:
`/restaurant/<int:restaurant_id>/`
`/restaurant/<int:restaurant_id>/menu/`
10. Create new menu item to add the the chosen restaurant:
`/restaurant/<int:restaurant_id>/menu/new/`
11. Edit a menu item (name, Description, price, and course type):
`/restaurant/<int:restaurant_id>/menu/<int:menu_id>/edit`
12. Delete a menu item from website database:
`/restaurant/<int:restaurant_id>/menu/<int:menu_id>/delete`
13. Display menu items as JSON file:
`/restaurant/<int:restaurant_id>/menu/JSON`
`/restaurant/<int:restaurant_id>/menu/<int:menu_id>/JSON`


## License
`Restaurants_Catalog` is a released under the [MIT License](https://opensource.org/licenses/MIT)
