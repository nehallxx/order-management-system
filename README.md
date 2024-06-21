# order-management-system
steps to setup
1- clone the repo:
   git clone (https://github.com/nehallxx/order-management-system.git) 
   and change to repo directory
   cd "order-management-system" 
2- install the following:
   npm install
3- open .env file and add the database
   e.g: DATABASE_URL="postgresql://user_name:passwrd@localhost:5432/order_management"
4- setup prisma:
   npx prisma migrate dev
   npx prisma generate
5- seed databse with data:
   npm run seed
6- run the app:
   npm run start
7- to test:
   a- add to cart:
   curl -X POST http://localhost:3000/api/cart/add -H "Content-Type: application/json" -d '{"userId": 1, "productId": 1, "quantity": 2}'
   b- view cart:
   curl http://localhost:3000/api/cart/1
   c- update:
   curl -X PUT http://localhost:3000/api/cart/update -H "Content-Type: application/json" -d '{"cartItemId": 1, "quantity": 3}'
   d- make order:
   curl -X POST http://localhost:3000/api/orders -H "Content-Type: application/json" -d '{"userId": 1}'
   e- get order with id:
   curl http://localhost:3000/api/orders/1
   f- update status of order:
   curl -X PUT http://localhost:3000/api/orders/1/status -H "Content-Type: application/json" -d '{"status": "SHIPPED"}'
   h- order history:
   curl http://localhost:3000/api/users/1/orders
   i- add coupon:
   curl -X POST http://localhost:3000/api/orders/apply-coupon -H "Content-Type: application/json" -d '{"orderId": 1, "couponCode": "DISCOUNT10"}'


NOTE: just make sure you fill in the tables with suitable data e.g userID, productId, etc.. 







