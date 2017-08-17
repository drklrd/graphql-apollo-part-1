```javascript

query {
    user(id: "23"){
        friends {
            company {
                name
            }
        }
    }

}

```

Rootquery is like entry point of data . RootQuery allows to jump at very specific node.


Resolve function resolves differences between incoming data model and datatype we are trying to use in graphQL


### Naming the query  :

```javascript

query findCompany{
    company(id : "1"){
        id
        name
    }
}

```


Multiple query for same type ....

```javascript

{

    apple : company(id : "1"){
        id
        name
    }

    google : company(id : "1"){
        id
        name
    }

}

```


### Query fragments... essentially just a list of properties we want to get access to.

```javascript

{

    apple : company(id : "1"){
        ...companyDetails
    }

    google : company(id : "1"){
        ...companyDetails
    }

}

fragment companyDetails on Company{
    id
    name
    description
}

```


### mutation

```javascript
mutation {
  addUser(firstName:"Mero",age:23){
    id
    firstName
    age
  }
}
```
