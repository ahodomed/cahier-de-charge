users {
  id int pk
  role_id int fk
  username string
  password_hash password_hash
  first_name string
  last_name string
  
}

address{
  id int pk
  user_id int fk
  address string
  city string
  email email
  postal_code string
  phone_number number
}

media {
  id pk
  product_id fk
  title string
  description string
  image_url string
  
}

products {
  id int pk
  category_id int fk
  name string
  description string
  price DECIMAL
  stock_quantity number
}

categories {
  id in pk
  name string
}

role{
  id int pk
  role_name string
}

}

users.id < adresse.user_id
products.id < medias.product_id
categories.id < products.category_id
role.id < users.role_id
