# Warehouse Management System

## Executive Summary

*The Warehouse Management System (WMS) will be deployed at a number of warehouse locations to aid employees in four categories and customers (detailed under **Business Objectives**) manage available product and make decisions based off that product.*

*The WMS will be broken down into four main components:*
1. *Warehouse Management Panel*
2. *Sales and Customer Panel*
3. *Delivery Panel*
4. *Management Panel*

Through these three, warehouse staff, delivery drivers, the sales force, branch managers, and customers will be able to efficently communicate and manage products stored at the warehouse location.

## Business Objectives

*The WMS will allow **Warehouse Staff** to manage both incoming and outgoing orders. They will be able to organize available product based off schmetics of the warehouse. Integration with their mobile devices will make accessing the WMS easy and remote.*

***Delivery Driver's** will automatically have all routes organized based off a number of different traffic and distance factors to maximize their efficency and number of routes. In addition driver's will have the same remote access the Warehouse Staff will have, making organizing and locating packages within their trucks as easy as possible.*

*The **Sales Team** will have the ability to create new customer accounts. In addition sales members will have the ability to request new orders and process/interact with their created customer accounts. The Sales Team will have a number of statistical information regarding the flow of products in-to and out-of the warehouse.*

***Customer** accounts will allow customers the ability to both request orders remotly from an online platform or through an on-site terminal at the warehouse's store-front. Customer request will be sent to their assigned sales representative. Customers will have the ability to create order bundles that allow them to group specific products together to make checking out quicker and more efficent.*

***Branch Managers** will have the ability to manage any portion of the system. In addition they will receive all new order request from sales representatives and warehouse staff. They will be able to create an account of any level and can manage any customers order request.*

*The application is required to run nativley for all users with the exception of Customer's who will have the ability access the platform remotley through a website.*

*While a majority of the computing should come from the devices the application is running on, a single server will be needed to act as a database for information regarding the warehouse. This includes all product information, diagnostic reports for all application instances, saved customer bundles, saved bundle templates, etc. This server does **not** have to be an onsite machine and can instead be outsourced to a third-party cloud provider.*

*The system should feature some network ability to allow multiple warehouse's to speak with one another if requested. The warehouses should be able to share available products with one-another and through a request, a warehouse could recieve product from another warehouse as a regular shipment.*

*While the warehouses will be conected, the **Branch Manager** of the source warehouse should be the only one able to manage that specific system.*

## Background

*The WMS will help speed up the process of product management for warehouses of all sizes by providing a single point of interaction for all functions found within the warehouse.*

*Its driving feature will be the ability to allow customer's to make bundled request of products and access their orders remotley speeding up the time it takes for them to get materials. In addition they will have on-site access through a terminal located in the warehouse's store-front; where a sales representative or front-counter associate can assist them.*

*Members of the warehouse's staff team will have access to statistical data providing information to the levels of product, the rate of in-flow-out-flow, product turn-over rate, and many other useful business things.*

## Scope

*The WMS is not an online retail store where contractors can purchase materials for future and ongoing projects. It is a system that gives warehouse staff members the ability to track products and allow customers the ability to make request for shipments as quickly and effortlessly as possible.*

*No request made by a customer is to be handled automatically. All request made for shipments will be routed to the customer's assigned sales representative. This will allow the sales representative to double check the product is available and schedule a time for delivery.*

*Delivery driver's will not have access to product information past what is loaded into their truck.*

## Functional requirements

***Warehouse Management Panel:** The Warehouse Management Panel (WMP) will serve as a point of access for warehouse staff members. Within this panel employees will be divided into two groups, Warehouse Staff and Warehouse Manager. **Warehouse Staff** will have the ability to move existing products within the system within the warehouse and to mark product as loaded on a delivery truck.*

*The **Warehouse Manager** will be able to manager all Warehouse Staff members and have the ability to request new shipments which are forwarded to the Branch Manager.*

***Sales and Customer Panel:** Through the Sales and Customers Panel (SCP) sales representatives will be able to contact customers directly and assist them with any questions or concerns. The SCP will allow sales represenatives to view information regarding the warehouses's available product.*

*Customers will have the ability to view the levels of available product and make request to their sales representatives for new shipments. In addition they will be able to create bundles of products that can be re-requested with one-click. Customer's should also be able to make inquires to the Branch Manager's regarding issues with request or the sales representative. Customer's can access the WMS remotley from an online web-panel (that tailors to both mobile and desktop platforms) or on-site through a terminal at the warehouse.*

***Delivery Panel:** The Delivery Panel (DP) will be the only portion of the WMS that resides soley on a mobile device. The DP will allow delivery driver's to organize their routes based off a number of different traffic conditions as well as internal factors from the warehouse (Ex: A delivery having priority over all others). Delivery driver's will be able to pull up information regarding an order when they arive at a delivery. This portion of the system will require the customer to sign into their account (or some other form of authentication, a pin?) and view the delivery selected by the driver. From here they can check off recieved products and mark the shipment as either complete or incomplete. Depending on the status:*

*1. **Incomplete:** The Warehouse Manager is informed of what products were not delivered. All other products are removed from the warehouse's database.*

*2. **Complete:** The products are removed from the warehouse's database.*

***Management Panel:** The Management Panel (MP) will provide branch managers and other authorized users with the ability to control all other conneted panels from one site. The management panel will be fed information from all other panels and allows the Branch Manager to make shipment request, interact with customer request, view available products, and other related information.*

*The MP will also allow Branch Managers to create new accounts of any type, or edit existing ones. The MP will also serve as the location to house configuration regarding the inter-warehouse network that warehouse's can use to communicate product levels, employees, customers, etc with.*


## Personnel requirements

*This project would ideally work with three developers to work on each of the three smaller panels (WMP, SCP, DP). The three would then collectivley work on the MP which would allow them the familiarity to make the system not four seperate parts, but one coexisting system.*

*The project should stem from the MP with that being the first item completed to provide a basis for the remaining three components.*

## Delivery schedule

***Phase One:** Demonstration of core MP. Ability to create multiple accounts from a root Branch Manager account. Simple basis for product inventory setup. The three developers should start work on their indavidual components.*

***Phase Two:** Core MP is complete and foundation for the other three components is set. Back-end at a bare minimum should be completely setup and ready for a frontend to be attached. This should include having the main data-server setup and ready to accept request. While the indavidual native platforms do not have to be complete, some skeleton should be for a demonstration.*

***Phase Three:** Project development complete, the project will now be loaded onto a single warehouse's solution for testing. At this point all warehouse's who **will** be getting the application should recieve documentation for all levels of interaction to familiarize the warehouse staff with the system.*

***Phase Four:** Project deploment. All application interfaces as well as backend data-server code is sent to the appropriate warehouse's to be setup on their infastructure. New equipment is purchased if nessicary to fit the applications needs. All staff accounts are created and sales representatives will be tasked with porting over all existing customer accounts.*

***Phase Five:** Continued improvement and maintance from the developers in response to the warehouse staff and their customers.*

## Other requirements

*The application should be accessible only from a native-ran application.*

*The only exception to the above is for the Customer Panel, Customer's will be able to access the application through a remote website that'll act as a messenger to the application itself. This is **not** a website for the customer to shop freely, but is instead a way for them to quickly make request for product without having to directly contact the sales representative.*

*The application will need to be made to run on native Apple/Android tablets and smartphones as well as Windows based desktop and laptops. The data-server should run on CentOS. All frameworks/languages/operating systems used should be up-to-date and used as defined in their respective documentations.*

*Due to the applications ability to communicate with other warehouse that is connected, the application should feature an OAuth server and client that will handle all request to/from another warehouse.*

## Assumptions

*This project will rely on a number of differnt frameworks/APIs/Languages detailed below:*

1. ***[Google Maps API](https://developers.google.com/maps/documentation/)** - Making routes for delivery driver's and prioritizing shipments.*
2. ***[OAuth2.0](https://oauth.net/2/)** - Authentication of request from other warehouse's.*
3. ***[Windows](https://www.microsoft.com/en-us/windows) 10 Operating System** - To be used to run the native application on desktop.*
4. ***[Apple](https://www.apple.com/)/[Android](https://www.android.com/) Phone/Tablet** - To be used by Warehouse and Delivery staff to manage products and customer orders; through a native application.*
5. ***[CentOS](https://www.centos.org/) (Linux)** - Container for data-server.*
6. ***[Oracle MySQL](https://www.mysql.com/)** - Ran on the CentOS data-server. Stores all data used by any of the instances of the native application.*
7. ***Backend Languages** - [Java](https://www.java.com/en/) for Windows and Android native applications. [Swift](https://swift.org/) for Apple products.*
8. ***Front-end Languages** - All front-end logic should be written in HTML, CSS, and Javascript using Google's [Angular](https://angular.io/) framework.*
9. ***Front-end Styling** - Front-end styling should conform to Google's [Material](https://material.io/) design standard. Usage of the provided [Angular Material](https://material.angular.io/) components is recommended.

## Limitations

*Due to there only being three developers, time is to be taken to ensure a reliable end product. The total timeline from start of **Phase One** until the continued integration of **Phase Five** is 4 months. This allows for a theoretical one-month-per-component. The timing in which each Phase is released is entirely due to the developers.*

## Risks

*Due to the lack of developer's time is a retraint. A bug that arises for one developer could need the help of another, haulting all progress on a component.*

*In addition new features may be requested from warehouse staff members and should be accounted for as they arise.*
