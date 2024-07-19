# MangoDB-Task

Queries:-

1.	Find all the information about each products

Ans: db.product.find()

2.	Find the product price which are between 400 to 800

Ans: db.product.find({product_price:{$gt:400,$lt:500}})

3.	Find the product price which are not between 400 to 600

Ans: db.products.find({ $or: [ { price: { $lt: 400 } }, { price: { $gt: 800 } } ] })

4.	List the four product which are greater than 500 in price 

Ans: db.product.find( {product_price:{$gt:500}}).limit(5)

5.	Find the product name and product material of each products

Ans: db.product.find({},{ product_name: 1, product_material: 1})

6.	Find the product with a row id of 10

Ans: db.product.find().skip(9).limit(1)

7.	Find only the product name and product material

Ans: db.product.find({},{product_name:1,product_material:1}).skip(9).limit(1)
8.	Find all products which contain the value of soft in product material 

Ans: db.product.find({product_material:{"$eq":"Soft"}})

9.	Find products which contain product color indigo  and product price 492.00

Ans: db.product.find({ "$or": [{product_color: "indigo" },{product_price: 492.00 }]})

10.	Delete the products which product price value are 28

Ans: db.product.deleteManey({ price: 28 })

