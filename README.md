# Pharmacy-Management-using-Mongodb

This is a simple Pharmacy Management System created using MongoDB. 

The system is composed of three main collections:

           1)drugs, 
           2)customers, and 
           3)orders. 
           
The drugs collection stores information about the drugs available in the pharmacy, including 

            1)name, 
            2)description, 
            3)quantity, and 
            4)price. 
            
The customers collection stores information about the customers, including

            1)name, 
            2)email, 
            3)phone number, and 
            4)address.
             
The orders collection stores information about the orders placed by customers, including

            1)date, 
            2)customer ID, 
            3)items purchased (drug ID and quantity), and 
            4)total price.

# Installation

1)Make sure you have MongoDB installed on your machine.

2)Clone the repository to your local machine.

3)Open a terminal and navigate to the project directory.

4)Start the MongoDB shell by running the command mongo.

5)Create a new database by running the command use pharmacy.

6)Create the necessary collections by running the commands db.createCollection("drugs"), db.createCollection("customers"), and db.createCollection("orders").

7)Insert sample data into the collections by copying and pasting the code from the pharmacy_mongodb.js file in the repository.

8)Start using the system by running queries against the collections.

# Usage

   The Pharmacy Management System allows you to perform various operations on the drugs, customers, and orders collections. Here are some sample queries to get you started:

1)Retrieve all drugs: 

         db.drugs.find()

2)Retrieve all customers: 

         db.customers.find()

3)Retrieve all orders: 

         db.orders.find()

4)Retrieve all orders for a specific customer: 

         db.orders.find({ customer_id: <customer_id> })

5)Retrieve all orders containing a specific drug: 

         db.orders.find({ "items.drug_id": <drug_id> })

6)Update the quantity of a drug: 

         db.drugs.updateOne({ _id: <drug_id> }, { $set: { quantity: <new_quantity> } })

7)Insert a new customer: 

         db.customers.insertOne({ name: <customer_name>, email: <customer_email>, phone: <customer_phone>, address: <customer_address> })

# Contributing

   Contributions are welcome! If you find a bug or have an idea for a new feature, please submit an issue or a pull request.
