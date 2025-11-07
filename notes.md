# Learning notes

## JWT Pizza code study and debugging

As part of `Deliverable ⓵ Development deployment: JWT Pizza`, start up the application and debug through the code until you understand how it works. During the learning process fill out the following required pieces of information in order to demonstrate that you have successfully completed the deliverable.

| User activity                                       | Frontend component | Backend endpoints | Database SQL |
| --------------------------------------------------- | ------------------ | ----------------- | ------------ |
| View home page                                      |                    |                   |              |
| Register new user<br/>(t@jwt.com, pw: test)         |                    |                   |              |
| Login new user<br/>(t@jwt.com, pw: test)            |                    |                   |              |
| Order pizza                                         |                    |                   |              |
| Verify pizza                                        |                    |                   |              |
| View profile page                                   |                    |                   |              |
| View franchise<br/>(as diner)                       |                    |                   |              |
| Logout                                              |                    |                   |              |
| View About page                                     |                    |                   |              |
| View History page                                   |                    |                   |              |
| Login as franchisee<br/>(f@jwt.com, pw: franchisee) |                    |                   |              |
| View franchise<br/>(as franchisee)                  |                    |                   |              |
| Create a store                                      |                    |                   |              |
| Close a store                                       |                    |                   |              |
| Login as admin<br/>(a@jwt.com, pw: admin)           |                    |                   |              |
| View Admin page                                     |                    |                   |              |
| Create a franchise for t@jwt.com                    |                    |                   |              |
| Close the franchise for t@jwt.com                   |                    |                   |              |


| User activity                                                            | Frontend component     | Backend endpoints                                        | Database SQL                                                                                                           |
| ------------------------------------------------------------------------ | ---------------------- | -------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| View home page                                                           | home.jsx               | --                                                       | --                                                                                                                     |
| Register new user  <br>([t@jwt.com](mailto:t@jwt.com), pw: test)         | register.jsx           | `[POST] /api/auth`                                       | INSERT INTO user(name, email, password) VALUES (?, ?, ?) INSERT INTO userRole (userId, role, objectId) VALUES(?, ?, ?) |
| Login new user  <br>([t@jwt.com](mailto:t@jwt.com), pw: test)            | login.tsx              | `[PUT]/api/auth`                                         |                                                                                                                        |
| Order pizza                                                              | menu.tsx               | ```[POST]/api/order```                                   |                                                                                                                        |
| Verify pizza                                                             | delivery.tsx           | ```[POST]/api/order/verify```                            |                                                                                                                        |
| View profile page                                                        | dinerDashboard.tsx     | --                                                       | --                                                                                                                     |
| View franchise  <br>(as diner)                                           | franchiseDashboard.tsx | ```[GET]/api/franchise/:userId```                        |                                                                                                                        |
| Logout                                                                   | logout.tsx             | ```[DELETE]/api/auth/```                                 |                                                                                                                        |
| View About page                                                          | about.tsx              | --                                                       | --                                                                                                                     |
| View History page                                                        | history.tsx            | --                                                       | --                                                                                                                     |
| Login as franchisee  <br>([f@jwt.com](mailto:f@jwt.com), pw: franchisee) | login.tsx              | ```[PUT]/api/auth```                                     |                                                                                                                        |
| View franchise  <br>(as franchisee)                                      | franchiseDashboard.tsx | ```[GET]/api/franchise/:userId```                        |                                                                                                                        |
| Create a store                                                           | createStore.tsx        | ```[POST]/api/franchise/:franchiseId/store```            |                                                                                                                        |
| Close a store                                                            | closeStore.tsx         | ```[DELETE]/api/franchise/:franchiseId/store/:storeId``` |                                                                                                                        |
| Login as admin  <br>([a@jwt.com](mailto:a@jwt.com), pw: admin)           | login.tsx              | ```[PUT]/api/auth```                                     |                                                                                                                        |
| View Admin page                                                          | adminDashboard.tsx     | ```[GET]/api/franchise?page=0&limit=10&name=*```         |                                                                                                                        |
| Create a franchise for [t@jwt.com](mailto:t@jwt.com)                     | createFranchise.tsx    | ```[POST]/api/franchise```                               |                                                                                                                        |
| Close the franchise for [t@jwt.com](mailto:t@jwt.com)                    | closeFranchise.tsx     | ```[DELETE]/api/franchise```                             |                                                                                                                        |

