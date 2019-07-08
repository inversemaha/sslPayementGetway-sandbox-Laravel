=== Plugin Name === Contributors: C.M.Sayedur Rahman
sayed@sslwireless.com Tags: Payment Gateway, SSLCommerz, IPN, Laravel
5.6 Requires : PHP 5.6 and Mysql License: GPLv2 or later

== Description == In this example you will find below script and a mysql
table creation file. 1. routes\web.php : Create route for the functions
2. app\Http\Controllers\PublicSslCommerzPaymentController.php: All the
functions to do the transaction. Read the comments carefully. 3.
app\Http\Controllers\SSLCommerz.php: Helping class, here you will input
store information 4. app\Http\Middleware\VerifyCsrfToken.php : Input
Route names to accept call from out side your site 5.
Sample\_order\_table.sql: This is a sample table to store order or
transaction information.

==Run the project== 1. First create your Sanbox(Test Environment) store
account from below url. After registration you will get two mail. One
for Store\_id and Store\_password.Another one for Report panel access.\
 https://developer.sslcommerz.com/registration/ Note: For live store id
or account you have to communicate with us. Our mail address:
operation@sslcommerz.com 2. Then give the store\_id and store\_password
in SSLCommerz.php page. 3. Here you have to run the
PublicSslCommerzPaymentController.php controller by calling pay(Like:
http://yourdomain.com/pay or http://yourdomain.com/public/pay) Here you
have to receive all the order data to initate the payment. Lets your
oder trnsaction informations are saving in a table called "orders" In
orders table order uniq identity is "order\_id","order\_status" field
contain status of the transaction, "grand\_total" is the order amount to
be paid and "currency" is for storing Site Currency which will be
checked with paid currency. 4. You have to set your IPN page from the
provided report panel. After login, go to My Stores then IPN Settings.
IPN url will be http://yourdomain.com/ipn or
http://yourdomain.com/public/ipn.

== Help URL== 1. https://developer.sslcommerz.com/docs.html :URL to
start integrate SSLCOMMERZ as a Developer 2.
https://developer.sslcommerz.com/registration/: URL to Create Account in
Sandbox
