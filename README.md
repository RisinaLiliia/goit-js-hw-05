# goit-js-hw-05

Task 1. User Names

Perform this task in the file task-1.js

Write an arrow function getUserNames(users) that will accept one parameter users — an array of user objects. The function should return an array of names of all users (the name property) from the users array.

Take the code below and insert it after the declaration of your function to verify that it works correctly. The results of its calls will be printed to the console.

console.log(
 getUserNames([
 {
 name: "Moore Hensley",
 email: "moorehensley@indexia.com",
 balance: 2811
 },
 {
 name: "Sharlene Bush",
 email: "sharlenebush@tubesys.com",
 balance: 3821
 },
 {
 name: "Ross Vazquez",
 email: "rossvazquez@xinware.com",
 balance: 3793
 },
 {
 name: "Elma Head",
 email: "elmahead@omatom.com",
 balance: 2278
 },
 {
 name: "Carey Barr",
 email: "careybarr@nurali.com",
 balance: 3951
 },
 {
 name: "Blackburn Dotson",
 email: "blackburndotson@furnigeer.com",
 balance: 1498
 },
 {
 name: "Sheree Anthony",
 e-mail: "shereeanthony@kog.com",
balance: 2764
},
])
); // ["Moore Hensley", "Sharlene Bush", "Ross Vazquez", "Elma Head", "Carey Barr", "Blackburn Dotson", "Sheree Anthony"]

Leave this code for your mentor to review.

What your mentor will look for when reviewing:

The variable getUserNames is declared
The variable getUserNames is assigned an arrow function with a parameter (users).
The map() method is used to iterate over the users parameter
A function call with the specified array of users returns the array ["Moore Hensley", "Sharlene Bush", "Ross Vazquez", "Elma Head", "Carey Barr", "Blackburn Dotson", "Sheree Anthony"]
A function call with random but valid arguments returns the correct value

Task 2. Users with a friend

Perform this task in the file task-2.js

Write an arrow function getUsersWithFriend(users, friendName) that will accept two parameters:

the first parameter users is an array of user objects
the second parameter friendName is the name of the friend to search for.
The function should return an array of all users from the users array who have a friend named friendName. Each user's friends are stored in the friends property. If there are no users who have such a friend, the function should return an empty array.

Tips:

You can use the filter() method to create a new array with elements that meet a certain condition.
Use the includes() method to check if the friends array contains friendName.
Take the code below and paste it after the declaration of your function to test that it works correctly. The results of its operation will be printed to the console.

const allUsers = [
 {
 name: "Moore Hensley",
 friends: ["Sharron Pace"]
 },
 {
 name: "Sharlene Bush",
 friends: ["Briana Decker", "Sharron Pace"]
 },
 {
 name: "Ross Vazquez",
 friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"]
 },
 {
 name: "Elma Head",
 friends: ["Goldie Gentry", "Aisha Tran"]
 },
 {
 name: "Carey Barr",
 friends: ["Jordan Sampson", "Eddie Strong"]
 },
 {
 name: "Blackburn Dotson",
 friends: ["Jacklyn Lucas", "Linda Chapman"]
 },
 {
 name: "Sheree Anthony",
 friends: ["Goldie Gentry", "Briana Decker"]
 }
];

console.log(getUsersWithFriend(allUsers, "Briana Decker"));
// [
// {
// name: "Sharlene Bush",
// friends: ["Briana Decker", "Sharron Pace"]
// },
// {
// name: "Sheree Anthony",
// friends: ["Goldie Gentry", "Briana Decker"]
// }
// ]

console.log(getUsersWithFriend(allUsers, "Goldie Gentry"));
// [
// {
// name: "Elma Head",
// friends: ["Goldie Gentry", "Aisha Tran"]
// },
// {
// name: "Sheree Anthony",
// friends: ["Goldie Gentry", "Briana Decker"]
// }
// ]

console.log(getUsersWithFriend(allUsers, "Adrian Cross" )); // []

Leave this code for a mentor to review.



What the mentor will look for when checking:

The variable getUsersWithFriend is declared
The variable getUsersWithFriend is assigned an arrow function with parameters (users, friendName)
The filter() method is used to iterate over the users parameter
If the value of the friendName parameter is the string "Briana Decker", the function returns an array of user objects with the names Sharlene Bush and Sheree Anthony
If the value of the friendName parameter is the string "Goldie Gentry", the function returns an array of user objects with the names Elma Head and Sheree Anthony
If the value of the friendName parameter is the string "Adrian Cross", the function returns an empty array
A function call with random but valid arguments returns the correct value

Task 3. Sorting by number of friends

Perform this task in the file task-3.js

Write an arrow function sortByDescendingFriendCount(users) that will take one parameter users — an array of user objects.

The function should return an array of all users sorted by the number of their friends (the friends property).

Take the code below and insert it after the declaration of your function to verify that it works correctly. The results of its operation will be displayed in the console.

console.log(
 sortByDescendingFriendCount([
 {
 name: "Moore Hensley",
 friends: ["Sharron Pace"],
 gender: "male"
 },
 {
 name: "Sharlene Bush",
 friends: ["Briana Decker", "Sharron Pace"],
 gender: "female"
 },
 {
 name: "Ross Vazquez",
 friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"],
 gender: "male"
 },
 {
 name: "Elma Head",
 friends: ["Goldie Gentry", "Aisha Tran"],
 gender: "female"
 },
 {
 name: "Carey Barr",
 friends: ["Jordan Sampson", "Eddie Strong"],
 gender: "male"
 },
 {
 name: "Blackburn Dotson",
 friends: ["Jacklyn Lucas", "Linda Chapman"],
 gender: "male"
 },
 {
 name: "Sheree Anthony",
 friends: ["Goldie Gentry", "Briana Decker"],
 gender: "female"
 }
 ])
);
// [
// {
// name: "Ross Vazquez",
// friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"],
// gender: "male"
// },
// {
// name: "Sharlene Bush",
// friends: ["Briana Decker", "Sharron Pace"],
// gender: "female"
// },
// {
// name: "Elma Head",
// friends: ["Goldie Gentry", "Aisha Tran"],
// gender: "female"
// },
// {
// name: "Carey Barr",
// friends: ["Jordan Sampson", "Eddie Strong"],
// gender: "male"
// },
// {
// name: "Blackburn Dotson",
// friends: ["Jacklyn Lucas", "Linda Chapman"],
// gender: "male"
// },
// {
// name: "Sheree Anthony",
// friends: ["Goldie Gentry", "Briana Decker"],
// gender: "female"
// },
// {
// name: "Moore Hensley",
// friends: ["Sharron Pace"],
// gender: "male"
// }
// ]

Leave this code for review by a mentor.

What the mentor will pay attention to when checking:

The sortByDescendingFriendCount variable is declared
The sortByDescendingFriendCount variable is assigned an arrow function with a parameter (users)
The toSorted() method is used to iterate over the users parameter
A function call with the specified users array returns a new array of users, sorted by the number of their friends in descending order
A function call with random but valid arguments returns the correct value

Task 4. Total balance

Write an arrow function getTotalBalanceByGender(users, gender), which will accept two parameters:

the first parameter users is an array of user objects,
the second parameter gender is a string that stores gender.
The function should use a method call chain and return the total balance of users (balance property) whose gender (gender property) matches the value of the gender parameter.

Take the code below and insert it after the declaration of your function to check that it works correctly. The results of its work will be displayed in the console.



const clients = [
 {
 name: "Moore Hensley",
 gender: "male",
 balance: 2811
 },
 {
 name: "Sharlene Bush",
 gender: "female",
 balance: 3821
 },
 {
 name: "Ross Vazquez",
 gender: "male",
 balance: 3793
 },
 {
 name: "Elma Head",
 gender: "female",
 balance: 2278
 },
 {
 name: "Carey Barr",
 gender: "male",
 balance: 3951
 },
 {
 name: "Blackburn Dotson",
 gender: "male",
 balance: 1498
 },
 {
 name: "Sheree Anthony",
 gender: "female",
 balance: 2764
 }
];

console.log(getTotalBalanceByGender(clients, "male")); // 12053

console.log(getTotalBalanceByGender(clients, "female")); // 8863

Leave this code for the mentor to review.

What the mentor will look for when reviewing:

The variable getTotalBalanceByGender is declared
The variable getTotalBalanceByGender is assigned an arrow function with parameters (users, gender)
The function body uses a chain of methods in the correct order
The value of the parameter users does not change
If the value of the parameter gender is the string "male", the function returns the number 12053
If the value of the parameter gender is the string "female", the function returns the number 8863
A function call with random but valid arguments returns the correct value
