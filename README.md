# TELCHISTES-3000
### Authentication Endpoints
The Authentication flow for the aplication is:

| METHOD | ENDPOINT             | TOKEN | ROLE  | DESCRIPTION           | POST PARAMS                  | RETURNS                 |
|--------|----------------------|-------|-------|-----------------------|------------------------------|-------------------------|
| POST   | /auth/singup         | -     | User  | User Singup           | `name`, `email`,`password`,  | { menssage: `string`, result: `token`} 
| POST   | /auth/login          | -     | User  | User Loging           | `email`, `password`          | { menssage: `string`, result: `token`} 

### User Endpoints

| METHOD | ENDPOINT             | TOKEN | ROLE  | DESCRIPTION           | POST PARAMS                         | RETURNS                 |
|--------|----------------------|-------|-------|-----------------------|-------------------------------------|-------------------------|
| GET    | /user                | yes   | adm   | Get All Users         |                                     | { menssage: `string`, result: `array`} 
| GET    | /user/:id            | yes   | adm   | Get One User          |                                     | { menssage: `string`, result: `object`} 
| GET    | /user/profile        | yes   | user  | Get One User          |                                     | { menssage: `string`, result: `object`} 
| PUT    | /user/:id            | yes   | adm   | Update One User       |`name`, `email`,`password`, `role`   | { menssage: `string`, result: `object`} 
| PUT    | /user/profile        | yes   | user  | Update own profile    |`name`, `email`,                     | { menssage: `string`, result: `object`} 
| PUT    | /user/password       | yes   | user  | Update own password   |`old password`, `new password`,      | { menssage: `string`, result: `object`} 
| POST   | /user                | yes   | ADM   | Create One User       |`name`, `email`,`password`, `role`   | { menssage: `string`, result: `object`} 

### Joke Endpoints

| METHOD | ENDPOINT             | TOKEN | ROLE  | DESCRIPTION           | POST PARAMS                  | RETURNS                 |
|--------|----------------------|-------|-------|-----------------------|------------------------------|-------------------------|
| GET    | /joke                | yes   | User  | Get all Jokes         |                              | { menssage: `string`, result: `array`} 
| GET    | /joke/:id            | yes   | User  | Get one Joke          |                              | { menssage: `string`, result: `object`} 
| POST   | /joke                | yes   | User  | Create  Joke          | `value`, `category_id`       | { menssage: `string`, result: `object`} 
| PUT    | /joke/:id/like       | yes   | User  | add Like to Joke      |                              | { menssage: `string`, result: `object`} 
| POST   | /joke/:id/favorite   | yes   | User  | add Like to Joke      |                              | { menssage: `string`, result: `object`} 






Instalado en este proyecto: adayvega@MacBook-Pro-de-Aday TELCHISTES-3000 % npm i express mysql2 sequelize nodemon dotenv bcrypt jsonwebtoken
