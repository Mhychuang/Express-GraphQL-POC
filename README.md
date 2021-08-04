# Express-GraphQL-POC
Prove of concept of Express-GraphQL
using the following scripts in http://localhost:5500/graphql GraphQL interface to perform CRUD. 

query getrestaurants{
  restaurants{
    name
    description
    dishes{
      name
      price
    }
  }
}

query getrestaurant($iid:Int = 1){
  restaurant(id:$iid){
    name
    description
  }
  
}

mutation editrestaurants($idd: Int = 2, $name: String= "Mike"){
  editrestaurant(id:$idd, name:$name){
    name
    description
  }
}

mutation setrestaurants{
  setrestaurant(input:{
    name: "New Restaurant",
    description: "American"}){
    name
    description
  }
}

mutation deleterestaurants($idd:Int =3){
  deleterestaurant(id: $idd){
    ok
  }
}
