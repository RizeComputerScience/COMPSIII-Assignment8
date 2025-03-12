# Assignment #8 - `PUT` and `DELETE` Requests

**TASK**: Continue to build on your `JSONPlaceholder` class from last week by implementing `PUT` and `DELETE` requests using the requests module. The class has the following class diagram:

![Assignment 8 Class Diagram](ClassDiagram.png)

The class is initialized with a `base_url` property that will be the endpoint where the requests are sent. The endpoint for this assignment should be [JSON Placeholder posts](https://jsonplaceholder.typicode.com/posts).

The class should have the following methods:
- `update_user(userId, title, body)`: Accepts a `userID`, `title`, and `body` as arguments. The method should then:
        - Create a dictionary that contains the `title` and `body`.  
        - Format the `base_url` to point to the specified `userId` endpoint (e.g. If the `userId` is 5 then then url would be `base_url/5`). 
        - Send a `PUT` request to the modified base_url with the dictionary data you created.
        - Return a dictionary with the (1) status code, (2) headers, and (3) first 500 characters in the response body.
- `delete_user(user_id)`: Accepts a `userID` as an argument. The method should then:
    - Format the `base_url` to point to the specified `userId` endpoint (e.g. If the userId is 5 then then url would be `base_url/5`). 
    - Send a `DELETE` request to the modified `base_url`.
    - Return a dictionary with the status code.

## Grading Your Work
This assignment can grade itself! To setup the autograding, you should do the following:
1. Clone this file to your local machine using the command
```bash
git clone PASTE_URL_HERE
```
2. Open the downloaded file in your VS Code editor.
3. In the left hand sidebar, press the "Testing" menu represented by the picture of a flask.
4. Click "Configure Python Tests".
5. You'll have two options to select. Select **pytest**.
6. Select the folder where the tests live. You can simply select `. Root directory`.
7. You can now run the tests by pressing the play icon. A passing test will get a ✅ and a failing test will get a ❌.
8. Run the tests as you code and by the end it should be all ✅ if you have followed the specifications for this assignment!

## Unit Test Explanations

Below is a summary of what each unit test for this assignment is checking for.

### Class Initialization Test
- `test_class_initialization`: Test if the class is initialized correctly with the `baseURL`

### `UPDATE` Requests Tests
- `test_update_user_success`: Tests successful `PUT` request to update a user using `update_user`.
- `test_update_user_correct_url_and_data`: Tests if `update_user` makes PUT request with correct URL and data.

### `DELETE` Requests Tests
- `test_delete_user_success`: Test successful `DELETE` request using `delete_user` method.
- `test_delete_user_correct_url`: Test if `delete_user` makes `DELETE` request with correct URL.