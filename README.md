# order-management-system
```steps to setup```
```
1- clone the repo:
   git clone (https://github.com/nehallxx/order-management-system.git) 
   and change to repo directory
```
```
  cd "order-management-system"
```
```
2- install the following:
   npm install
```
   
```
3- open .env file and add the database
   e.g: DATABASE_URL="postgresql://user_name:passwrd@localhost:5432/order_management"
```
```
4- setup prisma:
   npx prisma migrate dev
   npx prisma generate
```
```
5- seed databse with data:
   npm run seed
```
```
6- run the app:
   npm run start
```
```
 7- open any browser and paste this:
 http://localhost:3000/api
```
```
8- to test:
   a- add to cart:
      -navigate to POST /api/cart/add endpoint in CartController and click on it then click on (try it out)
      -fill in userId, productId,quantity.
      -click "Execute" to send request and see response.
   b- view cart:
      -navigate to GET /api/cart/{userId}
      -enter userId and click execute
   c- update:
      -navigate to PUT /api/cart/update
      -fill in cartItemId and quantity then execute
   d- remove from cart:
     - navigate to DELETE /api/cart/remove
     - enter the cartItemId then execute
   e- make order:
      -navigate to POST /api/orders
      -enter the userId and then execute.
   f- get order with id:
      - navigate to GET /api/orders/{orderId}
      - enter orderId then execute
   g- update order status:
   -navigate to PUT /api/orders/{orderId}/status
   -enter the orderId and new status value then execute
   h- view order history:
     - navigate to GET /api/users/{userId}/orders
     - enter userId and then execute
   i- apply coupon:
     -navigate to POST /api/orders/apply-coupon
     -enter orderId and couponCode then execute
```
