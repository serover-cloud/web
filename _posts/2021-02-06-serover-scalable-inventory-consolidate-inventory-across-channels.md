---
layout: post
title:  "Use Serover Scalable Inventory to enhance Customer Experience with accurate Inventory"
categories: [ Customer, Experience, Serover, AI ]
image: assets/images/customer-experience-4mp.jpg
featured: false
---
Serover Scalable Inventory makes it easy for Online Sellers to centralize inventory available to promise across all selling channels including external marketplaces e.g. Google, Walmart or Amazon. Never worry about keeping track of online inventory available to sell. 

Enterprises can integrate various systems to stream onhand supply, inbound supply and supply changes to Serover platform with REST API.  Selling channels and Order Management Systems (OMS) can integrate with Serover to stream all demands information and demand changes. Serover acts as a central inventory hub to process all supply and demand streams and calculate real-time inventory availability. Selling channels can obtain most up-to-date real time inventory available-to-promise (ATP) via ultra-fast REST apis (with millisecond latency) to show on product detail or checkout page, thus preventing underselling or overselling.  

Inventory ATP can be obtained either at a group level as aggregated value (inventory available for ecommerce ship to home orders) or at a store level (inventory available in store for BOPIS or curb side pickup)

Sellers can show real time inventory ATP for current on-hand as well as future inbound inventory to take planned backorder orders. OMS can also use future inbound inventory ATP to schedule backorders on a future date. 

Manage supply information
- Update Onhand and future inbound supply from various systems e.g. Stores, WMS or ERP
    - intelligently discard late messages

Reservations API
- Create reservations on cart items on checkout
- Get reservations
- Delete reservation once order is created
- Expire reservation if order is cancelled to unblock inventory

Manage demand lifecycle during fulfillment stages
- Reservation after checkout ( via create reservation API)
- Reservation consumed after order is confirmed (open demand allocated to a fulfillment location)
    - Reservation will be auto-canceled if not confirmed with order within 15 minustes (time is configurable)
- Inventory picked, packed and moved within warehouse/store ( demand processed at fulfillment location)
- Order shipped out from warehouse/store ( demand fulfilled ) resulted in decreasing the supplying as well as closing the demand

Available To Promise(ATP) API
- Get Available Inventory at aggregate level to show on product page or Ship To Home orders
- Get Available Inventory at location level for Buy Online Pickup at Store orders

Inventory Audit
- Audit stored in S3

ROI Success Metric
- Order cancelation metric ( to ascertain that cancelation due to incorrect inventory is reduced considerably)
- Backorder acceptance metric

(Features in Backlog)
- Dynamic Safety Stock for BOPIS and SFS : Predict store sales for each SKU at each location using advanced ML algorithms and determine buffer stock to fulfill orders from store
- Inventory audit dashboard 
- Inventory turnover metrics per site and aggregate
