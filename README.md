# Pagination-using-PHP-MySql-
Using Pagination to show 5 results per page


Create a table called pagination with 20 dummy fields; So $count will be = 20
-------------------------------------
$a = ceil($count/5);
Use ceil function to round the number UP to the nearest integer; Divided by 5 to have 5 results per page
-------------------------------------

anchor tag redirecting the clickable page buttons to the same page (pagination.php); Links with page number like 1 2 3 4 5 and so on, and the value of the number clicked (by GET) is sent 
-------------------------------------
	$page1=($page*5)-5;
Get the value of the page clicked on, by the anchor tag above, on the same page and store it in variable $page
If $page is empty or it's value = 1, set the value of $page1 as 0; else return $page1 = ($page*5)-5
-------------------------------------

'Selct query' on the table to display the contents for each page; limit the values using "$page1,5" so as to display only 5 results per page
