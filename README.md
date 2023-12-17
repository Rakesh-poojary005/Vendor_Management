# Vendor_Management
Vendor Management System with Performance Metrics

STEPS TO FOLLOW
1.Unzip the file 
  change directory cd into vendor_management
2. create virtual env
    python -m venv env
3. activate the environment:
    windows : env\scripts\activate
4.install necessary packages from req file
    pip install -r requirements.txt
5.Run the db commands
  python manage.py makemigrations
  python manage.py migrate
6.Create admin user
    python manage.py createsuperuser
    Default username : rakesh
            password : test
6. Token generation for api
    python manage.py drf_create_token rakesh

Once these steps are done , We are good to go with our api

API ENDPOINT - http://127.0.0.1:8000/api/vendors/ (post call to create new vendor)
while testing in postman goto headers add auth
Authorization : token generated for particular user
Request Body: Provide all the model fields
Repeat these steps for other api calls like get, put, delete


API ENDPOINT - http://127.0.0.1:8000/api/purchase_orders/ (post call to create new purchase)
while testing in postman goto headers add auth
Authorization : token generated for particular user
Request Body: Provide all the model fields
Repeat these steps for other api calls like get, put, delete

API ENDPOINT - http://127.0.0.1:8000/api/vendors/2/performance (get call to fetch perfoemance)

API ENDPOINT - http://127.0.0.1:8000/api/purchase_orders/1/acknowledge (post call to acknowledge purchase)





