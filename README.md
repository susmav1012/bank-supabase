# bank-supabase
Problem statement: To create a REST service that can fetch bank details, using the data given in the API’s query parameters. 
Using the data available in the repository in the backend DB.

******Case 1*******

==> Search API to return possible matches across all columns and all rows, ordered by IFSC code (ascending order) with limit and offset.
Request URL  - /api/search?q=Mumbai&limit=2&offset=1 

*******Case 2********

==>Branch API to return possible matches based on the branch name ordered by IFSC code (descending order) with limit and offset
Request URL  - /api/branch?q=LONI&limit=1&offset=1 

Procedure:
Create a nodejs application by creating a folder and running the following commands.
-->npm init
-->npm install express --save
-->npm install pg --save
After this node_modules folder will be created.
Follow the procedure in index.js
1) Import express,pg and bodyparser. Express is for creating API. pg is for adding postgreSQL database.
2) Use get() function from express to get the API and create a query for CASE 1 (/search/API). Return the rows that responds to the query.
3) Use get() function from express to get the API and create a query for CASE 2 (/branch/API). Return the rows that responds to the query.
4) Run using node <filename> or npm start

Push the project into GITHUB to deploy.

Run the project:
**************************
![image](https://user-images.githubusercontent.com/106637847/221558752-bb9e2e30-f6f7-4cd2-9ae2-4285c6b6d63a.png)

Deployed link:
***************************
https://backend-supabase.vercel.app/


Case 1 output:
***************************
http://localhost:3000/bankdetail/search?q=Mumbai&limit=2&offset=1
![image](https://user-images.githubusercontent.com/106637847/221741492-1ae3fa86-b35a-4d3b-987e-6ef0368794e4.png)

https://bank-supabase.vercel.app/api/search?q=Mumbai&limit=2&offset=1
![image](https://user-images.githubusercontent.com/106637847/221764505-5b5508d9-9a01-415f-b22c-c4df586a174e.png)


Case 2 output:
****************************
http://localhost:3000/bankdetail/branch?q=LONI&limit=1&offset=0
![image](https://user-images.githubusercontent.com/106637847/221741689-84d59fd5-f92f-41df-bf1e-ebbf5d5c6270.png)

https://bank-supabase-l6qd-k1kdoleew-susmav1012.vercel.app/api/branch?q=LONI&limit=1&offset=0
![image](https://user-images.githubusercontent.com/106637847/221763672-a67e67ec-9a34-4efe-839a-ec1f15b9fd66.png)


http://localhost:3000/bankdetail/branch?q=LONI&limit=1&offset=1
![image](https://user-images.githubusercontent.com/106637847/221741618-77076ec0-bf92-44eb-aeeb-65da8311048b.png)

https://bank-supabase-l6qd-k1kdoleew-susmav1012.vercel.app/api/branch?q=LONI&limit=1&offset=1
![image](https://user-images.githubusercontent.com/106637847/221764012-da147469-5859-4039-9489-e68a3e2953d5.png)



