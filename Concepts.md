2 or more protocols used in EV battery charging.

1. MQTT
2. OCPP etc.

-> OCPI allows for automated roaming between various EV charging networks.

key concepts

1. CPO - CPOs connect and operate smart EV chargers
2. EMSP - eMobility provide end user access to EV chargers
3. DSO - Energy distributor


Things to note -> 

1. EMSP provide a hub to avail the infrastructure where
we can connect to CP) (smart EV charger of our choice)

2. CPO may be any EMSP however it is not always the case.
just like I can have my own burger joint or I can serve in
a restaurant along with different burger joints.       

3. DSO - Distribution system operator is the energy supplier.

##What is OCPI? 
OCPI not to be confused with OCPP allows for an automated roaming between various EV charging networks.

let us understand some terms here...

##What is Roaming? 
In simple terms roaming refers to what petrol stations are for cars like EV to batteries.
It allows EV driver access to several charge point stations without 
worrying about the type of station or interface (ideally speaking or at least that is the goal of roaming).

Now there are a couple of things that come into picture.
EVs can have 2 types of battery module

1. Integrated battery module (~ like an onboard GPU)
2. Separate battery module 

-> Now what is the role of OCPI? 

OCPI is a standardization that is introduced to enable uniform interface for EMSPs, CPOs etc charging. 
It can be thought of as a RESTful API priciples for EV roaming. 

##What can be done using OCPI?
The fundamental thing that OCPI deals with is that it describes what are the paramters and data points that
an EMSP, CPO should capture so that energy is transferred to the customer and billing is paid. 
Apart from this it also discusses, session information, authentication, location information of battery, 
roaming hub, availability of a particular charger etc. 

With this we understand that OCPI offers us guidelines regarding EV roaming.

##What is OCPP?
OCPP (Open Charge Point Protocol) is a protocol that is followed when communicating between 
Charging management systems and Chargers. Not all Charging stations and chargers follow OCPP, 
there may be prorietary communication protocols or even other communication protocols like MQTT etc.
But those that are a part of OCA (open charge alliance) do follow OCPP.


There might be operators chosing to not go with OCPI over OCPP for several reasons.
This however causes vendor lock-in for EV operator. It might limit the EV operator
the choice to chose from the the availbe CPOs.Just like one can design their APIs to be SOAP over REST 
or even follow REST via websocket API.Which means companies can choose to still follow OCPI via MQTT or so. 
Any CPO utilizing OCPP will most definitely use OCPI as it makes sense for them to open up their business 
for wider customer base.


In that case an abstraction layer/interface would solve the issue, provided hardware compatibility exists.
This can be thought of as Phonepe or Paytm to banks or Bookmyshow to theatres or clear trip to
airlines for EMSPs to EV drivers.

##What problems one needs to solve when aspiring to become a middleware for (EMSPs+CPOs).
- Access to their infrastructure to communicate with our backend which in turn communicates with their backend.
- We manage billing + charging sessions + client interface for EV drivers.

###Merits
- You need not manage software.
- etc

###Demerits
- Control will be given to Energy aggreator

###Challanges
- How to convince CPOs and EMSPs?

For now let us assume that the business aspects of the problem are solved for the sake of arguments.