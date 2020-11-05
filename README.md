# Drill-Down-Report-in-Python

Case - Deep Dive Analysis													
													
Background:													
There are multiple instances where the Value Sales have decreased for different manufacturers in the last month compared to the month before that and it is important for the business to understand the exact area or level from where the drop is coming from													
													
Objective:													
To create a generic Python function which can do a deep dive analysis and give out exact focus area which are behind the cause of drop of Value Sales for a particular Manufacturer													
													
Steps to follow:													
1. Check if there is a drop in the Value Sales in the target month compared to last month													
2. If Step 1 shows an increase then print "There is no drop in the sales for a <particular manufacturer> in the <specified time period>" 													
3. If Step 1 shows a drop, then proceed by picking different deep dive options: Product level, Geographical level													
4. To do a deep dive on levels - zone,region,brand,subbrand													
5. calculate the growth rate of sales in the target month and contribution to overall value sales													
6. Take a product of the above two metrics to get a decisive metric which can then be sorted accordingly to get the actual focus area													
7. Expected final input to the function:													
	func(Manufacturer = "X", target_period = "May2019", reference_period = "Apr2019")												
8. Expected final output of the function:													
				Manufacturer	level	focus_area	growth_rate	contribution	product				
				X	Zone		    -                      20%	     50%	        -0.10				
				X	Zone		                          -30%	     10%	        -0.03				
				X	Zone								
				X	Zone								
				X	Subbrand								
				X	Subbrand								
				X	Region		                        -15%	      30%	         -0.05				
				X	Region								
				X	Brand		                          -25%	      5%	         -0.01				
				X									
													
Additional Information:													
1. There is a Geographical Level Hierarchy - Zone, Region													
2. There is a Product Level Hierarchy- Manufacturer, Brand, Subbrand, Item													
3. Pack Type and Pack Size are present under Item level													
4. Formula for growth_rate = ( Value Sales (focus_area) (target_period) - Value Sales (focus_area) (reference_period) ) * 100 / Value Sales (focus_area) (reference_period)													
5. Formula for contribution = Value Sales (focus_area) (target_period) * 100 / Value Sales (X) (target_period)													
6. Formula for product = growth_rate * contribution													
7. Focus Area can be any individual value of Geographical Level Hierarchy and Product Level Hierarchy. For example, North Zone, Urban, Brand 1, Subbrand 1										
