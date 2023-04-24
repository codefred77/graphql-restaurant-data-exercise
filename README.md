# graphql-restaurant-data-exercise

GraphQL Restaurant Data Exercise code. Part of Module 24, Full-stack development course

Query/Mutations code:

query restaurant ($Idd: Int = 2) {
  restaurant (id: $Idd) {
	  id
    name
    description
    dishes {
      name
      price
    }
  }
}

query restaurants {
	restaurants {
	  id
    name
    description
    dishes {
      name
      price
    }
    
	}
}
mutation setrestaurant {
  setrestaurant(input: {
    name: "Calafia",
    description: "Fusion fare combining Baja and Mediterranean cusines"
  }) {
    id
    name
    description
  }
}
mutation deleterestaurant ($idd: Int = 3) {
  deleterestaurant (id: $idd) {
    ok
  }
}
mutation editrestaurant {
  editrestaurant (id: 1, name: "New name") {
    id
    name
    description
  }
}
