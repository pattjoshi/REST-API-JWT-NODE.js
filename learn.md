# Rest APIs and jwt

- `npm init -y` initial npm.
- The is creating using node.js, express.js and mongoDB
- esm :- use for express code to react.js code.
- when you want to use this **config file**, you can import it like this:
  `import config from "./config";`
- All route in route folder
- in this file `router/index.js` I will import all the config files and export them as a single object
- read josn data in express `app.use(express.json());`
- ***

- **porcess.env.PORT** is the port that the server is running on the machine that is running the server script.
  - ` const PORT = process.env.PORT || APP_PORT;`

---

- becouse of export default, we can use this router in other files like this:
  - `import router from "./routes";`
  - we can use anather name instead of router
  - /api is the base route for all the routes in the routes folder so i use hear to defult all in routes
  - `app.use("/api", routes);`

---

### middlewares folder

- organize the code To create a centaral location of Error.
- we heandel the error in the _errorHendler_.js file
- if the error occer then we throw the error.
  `import { errorHandler } from "../../middlewares";`
- Decrease the size of import use index.js file inside the **middlewares folder**.
  - in this middleware we have 4 parameters
    - err is the error object
    - req is the request object
    - res is the response object
    - next is the next middleware function

---

### what is DEBUG_MODE: true

- we set DEBUG_MODE: true in .env file
- and we can see the error in the response

- joi :- it is a library, use for validation
- [JOI DOX](https://joi.dev/)
- 422 : Unprocessable Entity - validation error
- 401 :- unauthorised
- [verified the token](https://jwt.io/)
- Middleware req or res ke beech me kam kar ta he.
- Hash Password we use libriay `npm i bcrypt`
- `import bcrypt from "bcrypt";`
- `res.json({ msg: "This is the register route" });`

- Refresh toke expair date is high.

## Why we use app.use()

- app.use() is a function that takes a function as an argument and then calls it with the app as an argument.
- This is the same as app.get() or app.post() or app.put() or app.delete()

---

## How to resive what written in env file

- `npm i dotenv`
- import dotenv

```
import dotenv from "dotenv";
dotenv.config();

export const { APP_PORT } = process.env;
```

---

## img-1 SH512

<img width="843" alt="image" src="https://user-images.githubusercontent.com/78966839/183338023-3ac521b1-12ad-43f4-a9fd-fd5a5c8ea635.png">

## JWT HOW WOKR

- It store in clint side.
- is in 3 part
  - HEADER (red)
  - PAYLOAD (perple)
  - VERIFYSIGNATURE (blue)

#### HEADER:-

- algorithm

### PAYLOAD:-

- in payload show _role_ - _iat_ - _exp_

## SESSION

<img width="663" alt="image" src="https://user-images.githubusercontent.com/78966839/183339618-92938dab-a616-4dc7-8934-31d792bd7a9c.png">

## TOLEN BASED

<img width="621" alt="image" src="https://user-images.githubusercontent.com/78966839/183340043-8907a986-6ed5-4d4e-b77c-ec26fb231885.png">

# Todo for this project

- Register a user
- Login a user
- Who am i
- Add new Product
- Update a prodeuct
- Get all Products
- get single product
- Delete a product

### HOW TO START SERVER

`npm run dev`

```
 "dev": "nodemon -r esm  server.js",
    "start": "node -r esm server.js",
```

- Mentaning good qualati folder structure
-

## CRUD

- CREATE :- POST
- READ :- GET
- UPDATE :- PUT , PATCH
- DELETE :- DELETE

---

- PUT :- compit change
- PATCH :- specific path cahnge

---

- ! bang.

# Post master url for verify

- create 2 collaction.
  - Auth
  - PRODUCT

## inside **Auth** collaction

    - POST Register:-
          - url `localhost:5000/api/register`
          - Body , row, JSON
          - Defind like key & value
             ```
             {
               "name":"Om Prakash",
               "email":"om@gmail.com",
               "password":"secreate",
               "repeat_password":"secreate"
              }
             ```
    - POST Login:-
      - url `localhost:5000/api/login`
      - Body, row, JSON
      - Defind key & value pair (email, password)
      ```
      {
    "email":"om@gmail.com",
    "password":"secreate"

     }

````
   - GET Who am i (it show who is login)
       - url `localhost:5000/api/me`
       - Auth, Bearer Token , access token
       - it provide output
       ```
{
    "role": "customer",
    "_id": "62f914b9afe9eb3c28ceada8",
    "name": "Om Prakash",
    "email": "om@gmail.com",
    "createdAt": "2022-08-14T15:28:57.373Z"
}
       ```


## 1ST LOOK IN SIDE MONGO

<img width="950" alt="image" src="https://user-images.githubusercontent.com/78966839/183340642-547a5b86-db36-4336-a2d6-e7b1554780b1.png">

# [I LEARN FROM HEAR](https://www.youtube.com/watch?v=iM8h8-LcJPk&t=4586s)
````
