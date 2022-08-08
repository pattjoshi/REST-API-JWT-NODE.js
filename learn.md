# Rest APIs and jwt

- The is creating using node.js, express.js and mongoDB
- esm :- use for express code to react.js code.
- joi :- it is a library, use for validation
- [JOI DOX](https://joi.dev/)
- 422 : Unprocessable Entity - validation error
- 401 :- unauthorised
- [verified the token](https://jwt.io/)
- Middleware  req or res ke beech me kam kar ta he 
- add `unique: true` for automatic index.
-   **timestaps** :- the current time of an event that a computer records
-   `{ timestamps: false }`
-   
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

## Refrace token
- Long expairi data
- key:- are different
- it store in data base.
- 

` const refresh_token = JwtService.sign({ _id: user._id, role: user.role }, '1y', REFRESH_SECRET);`


******

<img width="661" alt="image" src="https://user-images.githubusercontent.com/78966839/183355495-ee0a135a-589f-4e1f-a807-4ea400f3d71f.png">



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

## 1ST LOOK IN SIDE MONGO
<img width="950" alt="image" src="https://user-images.githubusercontent.com/78966839/183340642-547a5b86-db36-4336-a2d6-e7b1554780b1.png">

## details of user Autantication Bear
<img width="876" alt="image" src="https://user-images.githubusercontent.com/78966839/183353567-6fdde027-e5fa-40dc-aa04-35ee91c1f0fe.png">


## sand request toke and get access token
`localhost:5000/api/refresh`


deloeteone ({toke: reqe.bidy.refracr.token}(






# [I LEARN FROM HEAR](https://www.youtube.com/watch?v=iM8h8-LcJPk&t=4586s)
