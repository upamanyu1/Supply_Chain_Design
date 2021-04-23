The management of New England Root Distributers decided to consolidate operations in a modern new facility. They selected Scranton Pennsylvania as the site of the new plant. This was a controversial decision as NERD root beer had always been manufactured in New England. However, the higher labor costs in New England drove them to re-locate the manufacturing operations. The new plant, located several hundred miles away from the New England market. It was part of a larger initiative within NERD to expand its sales. NERD’s market share for the regions outside of New England has grown significantly over the last 20 years. The Scranton plant is considered a major success not only in terms of opening new markets, but also in its lower operating costs, higher and more consistent quality, and ability to scale with growing demand.
Others view it as costly and a duplication of facilities. The project wants to answer analytic questions 
1) Does NERD have the right number of DCs in New England now? Should they be reduced?
 2) Should NERD source from the Bellows Falls, Vermont plant (BFP)? 
3) Does the current DC configuration provide sufficient level of service? 
4) Can the current configuration handle increases in demand?

![image](https://user-images.githubusercontent.com/40518603/115831876-caeed500-a42f-11eb-83cc-4c0286167d77.png)

 






Data
Distance DC to RDC 
Distances (in miles) between the five DCs and the twelve RDCs are in the screenshot of excel below. The distance includes the expected delivery distances from that RDC to its local customers.

![image](https://user-images.githubusercontent.com/40518603/115831944-e22dc280-a42f-11eb-9915-1e6eed93af15.png)

In the screenshot below  
1) Fixed cost and variable cost at Distribution centers is given. 
2) The Inbound transportation cost (The cost of moving a barrel from the plant to DC)
3) The Quantity demanded at the RDC and at DC.
 
![image](https://user-images.githubusercontent.com/40518603/115831974-ef4ab180-a42f-11eb-9880-1411bf641e95.png)
![image](https://user-images.githubusercontent.com/40518603/115832035-06899f00-a430-11eb-909e-d936e380aed1.png)

 

 Building the Model
We find the following things::
1)	The DC fixed cost = Fixed Cost  * DC Open
2)	OB transportation cost = Decision Variable * Distance Matrix * Cost per mile for barrel
3)	IB cost (transportation cost from Plant to DC) =  Decision variable(barrels produced in plant) * Cost per mile for barrel 
4)	Manufacturing Cost = Decision variable(barrels produced in plant) * Variable Cost(cost per barrel at each plant)
5)	DC Handling = Variable Cost * Quantity demanded
6)	At RDC Quantity Delivered >= Quantity Demanded
7)	DC Open is binary variable

![image](https://user-images.githubusercontent.com/40518603/115832089-14d7bb00-a430-11eb-909c-cfd380f99ca1.png)
![image](https://user-images.githubusercontent.com/40518603/115832107-1d2ff600-a430-11eb-945f-46b2d5152806.png)
![image](https://user-images.githubusercontent.com/40518603/115832141-27ea8b00-a430-11eb-9d97-7da8853055a4.png)

 


 
Based on the Data for Baseline flow and according to various policies we solve the model based on MILP Linear Programming can determine the total cost incurred by various adherence to different policies and display it in a chart form.

![image](https://user-images.githubusercontent.com/40518603/115832174-3638a700-a430-11eb-8713-b296570b0167.png)







