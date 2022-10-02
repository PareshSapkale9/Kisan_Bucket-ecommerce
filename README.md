# Ecommerce site made with React with Springboot MVC 
The ecommerce (Kisan Bucket) project. Built with ❤︎ by Paresh Sapkale©

![home](https://user-images.githubusercontent.com/101621564/193438246-16601431-a909-4e4d-a78f-b07f9b37633f.png)


# 📃Table of Contents
* Technologies
* Features
* How to run
* Future Work

# 👩‍💻Technologies
* React
* Bootstrap 
* MySql
* Springboot


# 😊Features
* List Products
* Add products to Cart
* Add product by seller
* Admin control

# 👷 How to run
## On React  

* create the new react application
```
npx create-react-app Kisan Bucket
cd Kisan Bucket
npm start
```
### Add some npm dependency

#### 🌟React lib
* Intall axios: (promise-based HTTP Client for node.js and the browser aka middleware) 
```
npm install axios
```
* Install Cors: (allows you to make requests to the server)
```
npm install cors
```
* Install React DOM: (entry point to the DOM and server renderers)
```
npm install react react-dom
```
* Install react-paginate:
```
npm install react-paginate --save
```
* Install React Redux (building the user interface)
```
# JS
npx create-react-app my-app --template redux
```

*Intsall web-vitals (shows how your pages perform, based on real world usage data)
```
npm install web-vitals
```
#### ✨For Design Purpuse (UI/UX)
* Install bootstrap npm 
```
npm install bootstrap@v5.2.1 
```
* Sweetalert (replace alert prompt) { Ref URL :https://sweetalert2.github.io/}
```
npm install sweetalert2
```
#### 🧾For database connectivity


* Install MySQL
```
npm install mysql
```
## On MySQL 
* create new database
```
create database KisanBucket
use KisanBucket

than leave it ..... remain at work until spring hibernates to create a table.
```
## On STS (Spring Tool Suite 4)

* In file > Open Project File System > select (KisanBucket_backed) on dir > Finish .

* When PRoject added succesfully added Right click the project > goto Maven > Update project > tick on Force updtae of snapshot/release . 
* Now u good to go run as Springboot App 

    ### ⭐Check out src/main/resource
    * In > application.properties
        * spring.datasource.username="your user"
        * spring.datasource.password="your pass"
    * In your machine create the directory as:
        * D:/server/uploads
        (For disk.upload.basepath)

# 🧡Future Work 
* added register page Firebase validation by otp / email
* added centralize page translation by i18next(Internationalization )

#  🐛 Issues
Some Page translation work is on pending so react router dom not access it on browser dev side... stay tune for that im uploading data soon as possible!!!

