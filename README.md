1. db.buyers.aggregate([{$group:{_id:"$address.city"}}])

2.  db.buyers.aggregate([{$group:{_id:"$address.zip"}}])

3. db.orderdetails.aggregate([{$group:{_id:"$order_id"}},{$sort:{_id: 1}}])

4.  db.orders.aggregate([{$group:{_id:"$customer_id"}}])

5. db.payments.aggregate([{$group:{_id:"$paymentMethod"}}])

6. db.payments.aggregate([{$group:{_id:"$paymentstatus"}}])

7. db.products.aggregate([{$group:{_id:"$category_id"}}])

8. 

9. db.orders.aggregate([{$group:{_id:"$status",OCount:{$count:{}}}},{$limit:3}])

10. db.payments.aggregate([{$match:{paymentstatus:"success"}},{$project:{amount:1}}])

11. db.products.aggregate([{$sort:{quantity:1}},{$limit:1},{$project:{name:1}}])
