# Chat-App
A real-time chat application, that enables users to communicate with other users in real-time, using Socket.IO. Integrated emoji sharing and profile image customization with Avatars fetched using Multiavatar API.

# Api Documentation (Chat-App):


### 1. **Register to Chat-App**

  ```http
  POST /auth/register
  ```
- Row body structure for a post request of file attchment :

  | Parameter      | Type               | Required  | Description              | Default |
  | :------------- | :----------------- | :-------- | :----------------------- | :------ |
  | `userName`         | `text`           | **true**  | User Name  | -       |
  | `email`         | `text`           | **true**  | User Email  | -       |
  | `password`         | `text`           | **true**  | User Password  | -       |
 
- Example for post request through **Postman** [form-data] (using a local storage file)

  | Key     | value |
  | :------ | :------ |
  | userName |    Ankita     |
  | email |    ankitgur03@gmail.com     |
  | password |    password     |

- Example Response on success **(status code 201)**
  ```javascript
  {
    "user": {
        "userName": "Ankita",
        "email": "ankitgur03@gmail.com",
        "password": "$2b$10$yeQhsGo4Tb9LhAwnsVUIfO2a2wOejEAE.DKS6pGtMe0IJUOH3KCIC",
        "isAvatarSet": false,
        "avatarPicture": "",
        "_id": "64b9755689d4591068d89fef",
        "createdAt": "2023-07-20T17:56:38.029Z",
        "updatedAt": "2023-07-20T17:56:38.029Z",
        "__v": 0
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY0Yjk3NTU2ODlkNDU5MTA2OGQ4OWZlZiIsImlhdCI6MTY4OTg3NTc5OH0.zMCtOLl81TIOB4vb8VA30IxOtv6c3s5ZrQIfPaBBV-E"
}
  ```

### 2. **Login to Chat-App**

  ```http
  POST /auth/login
  ```
- Row body structure for a post request of file attchment :

  | Parameter      | Type               | Required  | Description              | Default |
  | :------------- | :----------------- | :-------- | :----------------------- | :------ |
  | `userName`         | `text`           | **true**  | User Name  | -       |
  | `password`         | `text`           | **true**  | User Password  | -       |
  
- Example for post request through **Postman** [form-data] (using a local storage file)

  | Key     | value |
  | :------ | :------ |
  | userName |    Ankita     |
  | password |    password     |

- Example Response on success **(status code 200)**
  ```javascript
  {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY0Yjk3NTU2ODlkNDU5MTA2OGQ4OWZlZiIsImlhdCI6MTY4OTg3NTkyOX0.3EB3EMeUXVC8hN6nGYi9lxoSI7I3mpWL-8aSwEJjc7Y",
    "user": {
        "_id": "64b9755689d4591068d89fef",
        "userName": "Ankita",
        "email": "ankitgur03@gmail.com",
        "password": "$2b$10$yeQhsGo4Tb9LhAwnsVUIfO2a2wOejEAE.DKS6pGtMe0IJUOH3KCIC",
        "isAvatarSet": false,
        "avatarPicture": "",
        "createdAt": "2023-07-20T17:56:38.029Z",
        "updatedAt": "2023-07-20T17:56:38.029Z",
        "__v": 0
    }
}
  ```

