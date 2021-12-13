---
layout: case
title: Lab4 Case Discription
image_path: ""
thumb: lab4.jpg
main-pic: Display of order and delivery information.png
summary: Quam temere in vitiis, legem sancimus haerentia. Plura mihi bona sunt, inclinet, amari petere vellent. Ambitioni dedisse scripsisse iudicaretur.
nav-class: case-studies
permalink: case-studies/two/
date: 2021-12-12 4:23:00 -0600

---


> The main function of the application we designed is to simulate the whole process of ordering and delivering food to customers. The function of the app on the web side is to receive orders from customers and deliver the dishes to the specified customers, and the current customer ends the disconnection when the customer's desired dish is finished. When the page is open, the application will keep running, and the server will broadcast and web html update information when the customer enters, leaves, and receives the dishes.

>When multiple customer pages are opened, multiple customer connections will be generated. If the web side (not the server) is open, the customer will order immediately after the connection is successful, and if the web side is not open, the customer will order after clicking the "open" button after the web side is connected.

>For customer, since the customer may recall more than one delivery message, in order to prevent the recorded data from being manipulated at the same time, it is necessary to use a lock so that the corresponding variables cannot be used until the processing of the current message is finished, and then release the lock after the operation is completed.

> For client.js, it represents a restaurant and is used to handle the order and delivery operations of the corresponding customer, so it needs to store the corresponding dishes of the customer, the dishes waiting for delivery, and the dishes already delivered, in order to distinguish the status of different customers' dishes and the status of the dishes.

>For server.js, it is responsible for message forwarding, processing, and the management of clients connections. It needs to record the connected clients and the corresponding names for broadcasting when the clients join or disconnect.
