#Siametrics Backend Testing

## Algorithm Testing
##### 1. What is Big(O) of this function, and show how to calculate
```
function search(array, item) {
    let minIndex = 0;
    let maxIndex = array.length - 1;
    let currentIndex;
    let currentElement;

    while (minIndex <= maxIndex) {
        currentIndex = Math.floor((minIndex + maxIndex) / 2);
        currentElement = array[currentIndex];

        if (currentElement < item) {
            minIndex = currentIndex + 1;
        }
        else if (currentElement > item) {
            maxIndex = currentIndex - 1;
        }
        else {
            return currentIndex;
        }
    }
    return -1;
}
```
## SQL Testing
##### 1. Write a SQL query to get the second highest salary for each department from the Employee and Department table.
```
Employee Table
+----+--------+ -------------+
| Id | Salary | DepartmentId |
+----+--------+ -------------+
| 1  | 100    |       1      |
| 2  | 200    |       1      |
| 3  | 300    |       2      |
| 4  | 400    |       2      |
+----+--------+--------------+

Department Table
+----+--------+ ----+
| Id | Name         |
+----+--------+ ----+
| 1  | Finance      |
| 2  | Development  |
+----+--------+-----+
```
For example, given the above Employee table, the query should return 200 as the second highest salary. If there is no second highest salary, then the query should return null.
```
Output
+---------------------+--------+
| Department Name     | Salary |
+---------------------+--------+
| Finance             | 100    |
| Development         | 300    |
+---------------------+--------+
```

## Database Testing

##### 1. Please explain what is the best situation to use NoSql or Sql
##### 2. Create a Class Diagram for Food Delivery Service according to below instruction.

1. Food delivery has 2 user type, first one is Rider and second one is Customer.
2. Clearly that Customer can order a food but don't forget that Rider can also order the food as well.
3. Attribute for Rider is name, phone, username and rating score
4. Attribute for Customer is name, phone, username
5. One order is contains restaurant name, food name, customer who order the food, rider
