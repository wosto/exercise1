# exercise1

Original requirements:

Create a single page application that displays a list of items. 

These items must include a picture and a description.

The application functionality should satisfy the next use cases:
1. The user should be able to sort the items on the list using a drag and drop functionality.
2. There should be a counter in the page that shows how many items are being displayed.
3. Each item should have the actions: edit and delete. Edit allows a user to update the image of an item and the description text. Delete allows a user to remove an item from the list and update the counter.
4. A functionality to add a new item should exist. This functionality consist on a form to upload an image (jpg, gif and png extensions of 320px x 320px size) and a description text (max chars 300).
5. All the actions of the application should be done without refreshing the page (sort, add, edit and delete) and saved immediately.
6. On a page refresh action, it should be displayed the last state of the list.

Tools to be used for the development: vanilla JavaScript with jQuery (or any other js library) with any plugin and html5, css3, sass or less, any type of DB (if needed), any type of backend/language (if needed).

You CANNOT use a JavaScript Framework like: angularjs, react, riot, vue.js, etc.

Submit the application to a git repository with the necessary installation/execution instructions.

All documentation and comments in code should be in English

IMPORTANT: for trademark reasons; file names, repository name or any other asset of the current exercise SHOULD NOT contain the terms: "fanbridge" or "stensul". Please use ANY OTHER term than the previously mentioned.

------

With regards to the above, in order to create a self-packaged application, Web SQL (SQLite) was used as the local DB engine. LocalStorage and a serialised JSON object was also an option, although SQL gives a higher and more flexible scalability. With this approach, a server-side process was avoided, thus the image scaling is done via CSS only.

The image is stored as a Base64 encoded string in the items table, as well as the description. Each edit, delete and sort operation refreshes the table so that every change is tracked in real-time. The Data URL functionality has a limitation in IE (not Edge) of 99kb, but this limitation is not significative as for the objective of the exercise. Cancelling a recently created empty-item derives in deleting the item, to avoid orphan/empty items in the list. An empty item can be saved, nonetheless, and the descripcion placeholder will be displayed (this functionality can be changed if requested).

Installation/Run instructions:

1 - Open the HTML file in a Web Browser

-------
