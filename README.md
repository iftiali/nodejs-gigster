# Gigster QA Practical: Automated web application testing
by Iftikhar (iftiali@gmail.com)

Adding Chai and Mocha unit testing framework
Please see accompanying practical description for tasks.

### To run locally:
Please use sudo or root user to execute the following command. Also look at the error and make sure you have the correct name directory is present on local drive
```shell
  $ docker-compose up #starts server at 0.0.0.0
  
```

### Routes:
| Endpoint | Method | Input | Output |
|---|---|---|---|
| /user | POST | `{ username: string, password: string, isAdmin: bool }` | `{ username: string, isAdmin: bool }`
| /user/auth | GET  | `{ username: string }` | `{ username: string, isAdmin: bool }`
| /user/login | POST | `{ username: string, password: string }` | `{ username: string, isAdmin: bool }`
| /user/logout | POST | null | null |
| /expense | POST | `{ datetime: date, amount: number, description: string, owner: string }` | `{ datetime: date, amount: number, description: string, owner: string, id: string }`
| /expense/:id | GET | null | `{ datetime: date, amount: number, description: string, owner: string, id: string }`
| /expense/:id | PUT | `{ datetime: date, amount: number, description: string, owner: string }` | `{ datetime: date, amount: number, description: string, owner: string, id: string }`
| /expense/:id | DELETE | null | `{ datetime: date, amount: number, description: string, owner: string, id: string }`
| /report?start=<date>&end=<date> | GET | null | `[]{ datetime: date, amount: number, description: string, owner: string, id: string }`
