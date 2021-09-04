# Next JS ( FullStact Framework )

<hr/>

# Imam Group Catalog

<hr/>

## Class diagram

```plantuml
' left to right direction
skinparam linetype ortho

class User{
    -intger id
    -string name
    -string email
    -string password
    -datetime created_at
    -datetime updated_at
}

' type: FOOD, NON_FOOD, MIX
class Category{
    -integer id
    -string code
    -string name
    -string arabic_name
    -string hebrew_name
    -string alternate_name
    -string parent
    -integer category_lvl
    -boolean active
    -string type
    -integer importance_value
    -datetime created_at
    -datetime updated_at
}

class Product{
    -integer id
    -string code
    -string name
    -string display_name
    -string arabic_name
    -string hebrew_name
    -string alternate_name
    -string barcode
    -float price
    -float weight
    -string weight_unit
    -integer box_quantity
    -boolean new
    -string note
    -boolean active
    -string background_color
    -datetime created_at
    -datetime updated_at
}

' type => in_weight (example: 1kg => 20 NIS), in_quantity (example: 3 => 20 NIS), price (example: old_price => new_price)
class Offer{
    -integer id
    -string type
    -float price
    -float weight
    -float quantity
}

class Offer_Product{
    -integer id
    -integer offer_id
    -integer product_id
}

class Category_Product{
    -integer id
    -integer category_id
    -integer product_id
    -datetime created_at
    -datetime updated_at
}

class Favorite_Product{
    -integer id
    -integer user_id
    -integer product_id
}


class Product_Image{
    -integer id
    -integer product_id
    -string image
    -string image_name
    -datetime created_at
    -datetime updated_at
}

class Category_Image{
    -integer id
    -integer category_id
    -string image
    -string image_name
    -datetime created_at
    -datetime updated_at
}

Category --> Category
Category_Product --> Category
Category_Image --> Category
Category_Product --> Product
Product_Image --> Product
Favorite_Product --> Product
Favorite_Product --> User
Offer_Product --> Product
Offer_Product --> Offer

```

<hr />
