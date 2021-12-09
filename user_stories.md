1. As a kitchen worker, I need to see the current stock levels of our supplies so I can make decisions about ordering

* Given a supply, a user can see its current stock level
* A user can see a list of all current stock levels

2. As a kitchen worker, I need to modify the stock levels of our supplies so I can keep our records up to date

* A user can increase the stock level of an item
* A user can decrease the stock level of an item
* A user can set the stock level of an item to 0

3. As a kitchen manager, I need to know when stock levels get too low so I can resupply

* A user can set a threshold for a stock level
* When a stock level drops below the a set threshold, an email is sent to `stock@galvanize-restaurant.com`
* A user can change a threshold
* A user can remove a threshold

4. As a kitchen manager, I need my supplies automatically reordered when stocks get low so I can focus on other tasks

* A user can set a threshold for a stock level
* When a stock level drops below a set threshold, a correctly-formatted POST request is sent to `https://api.industrialsupply.com`
* A user can change a threshold
* A user can remove a threshold

---

The most immediately useful thing for the kitchen is to see what their current supply levels are, even if the levels have to be input directly into the system. Conversely, if a user can modify values but can't see them, no value is being provided. Once the user can see values, having an interface for modifying the values is the next most valuable thing because it's a simple step toward making the app interactive. At that point, it's more useful than a paper form. Automatic reordering likely provides more value than the alert, but most of the work of developing the alert is a dependency for automatic reordering and can provide value quicker.
