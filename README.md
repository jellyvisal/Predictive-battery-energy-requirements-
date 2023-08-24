<table>
<td><img src="https://github.com/jellyvisal/Predictive-battery-energy-requirements-/assets/142890460/58f213ee-3f46-4051-acc8-d8587d25cb9b"  width=500 /></td>
<td><p><h1>EV-Battery energy requirements and heat dissipation requirements </h1></p>
<p> Improve range, performance, and battery life by designing a battery pack considering a high-fidelity model and correlating the results with relevant theory.</p>
</table>

## Motivation and Results: 
Designing an energy-efficient and thermally optimized battery pack is crucial for various applications, from electric vehicles to renewable energy storage systems.
The energy requirements for a battery pack and the associated cooling requirements are closely interconnected, as both factors impact the overall performance, 
safety, and longevity of the system. We can observe that we have designed the battery pack requirements and specs needed for further calculations from the manufacturer.
We also understand the impact of these characters on the battery performance characteristics and safety aspects. 

## Difficulty level
Bachelor's

## Energy Requirements for Battery Pack:

The energy requirements of a battery pack depend on the intended application and the desired operational parameters. The Excel sheet called "Tataace1.5Ton" contains the vehicle dynamics calculations and heat generated in the battery pack during the drive cycle. The Drive cycle chosen for the experiment is WLTP Class 1; WLTP is an international driving cycle standard and is known for its rugged nature and extreme simulation conditions. 
Here are the key reasons why the WLTP drive cycle is considered harsher:

Realistic Driving Conditions: The WLTP drive cycle incorporates a broader range of driving scenarios that are more representative of real-world driving conditions. This includes a mix of urban, suburban, and highway driving, as well as variations in speed, acceleration, and deceleration. 

Higher Average Speeds: The WLTP drive cycle includes higher average speeds compared to the NEDC. This is significant because higher speeds typically lead to increased aerodynamic drag and greater energy consumption. 

Aggressive Acceleration and Deceleration: The WLTP drive cycle includes more aggressive acceleration and deceleration events, which better simulate real-world driving behaviors. Rapid acceleration and deceleration have a direct impact on fuel consumption and emissions, and including these events in the test cycle provides a more accurate representation of how vehicles perform in everyday situations.

Longer Test Duration: The WLTP drive cycle has a longer overall test duration compared to the NEDC. This longer test time allows the engine and vehicle systems to reach stable operating conditions, leading to more accurate measurements of fuel consumption and emissions.

Dynamic Load Variations: The WLTP drive cycle considers variations in vehicle load, including the number of occupants and cargo. This accounts for the impact of added weight on fuel efficiency and emissions, which is particularly important for real-world scenarios where vehicles are often used with varying load levels.

The drive cycle for WLTP class 1 is as follows for the time vs. speed plot. It was obtained using simple plot commands in MATLAB 


![image](https://github.com/jellyvisal/Predictive-battery-energy-requirements-/assets/142890460/e52fad49-4cba-48b9-844a-af3b1e9a5ad8)



## Suggested Prerequisites 

1) 	Study the [EV battery model documentation](https://www.mathworks.com/help/physmod/hydro/ug/sscfluids_ev_battery_cooling.html)
2) 	Go through [Xengineer Electric Vehicles tab and learn EV battery concepts and documentation](https://x-engineer.org/category/automotive-engineering/vehicle/electric-vehicles/)
3) 	Go through Excel sheet calculations and correlate them with relevant theory
4) 	Go through [WLTP class requirements](https://dieselnet.com/standards/cycles/wltp.php)

## Guide through the project 
1) Open the MATLAB Code called "PROJECT.mlx" and load the workspace variables that are named with file extension .mat 
2) While importing select the column vector tool or use the first part of the code to convert the table into a double format using table2array
3) Open the "Tataace-1.5Toninternshipreport.xlsx" file and go through the initial calculations.
4) Sheet 1 contains values for generic energy requirements and peak and minimal conditions
5) Sheet 2 contains the proper energy requirements as per [Xengineer documentation](https://x-engineer.org/ev-design-energy-consumption/).
    Here we can see that to move the energy for one Kilometer we require 0.237 Wh/km Hence the total energy requirement for the EV vehicle to attain a theoretical range of 100 Km we simply multiply the 100 * 0.2379 to get 23.79 kWh battery power requirement for this vehicle to get 100 km range as per the WLTP class 1 cycle. 
7) Sheet 3 contains heat generated by the battery in Watts throughout the WLTP cycle with a simple formula of i^2*R and the number of cells
8) The number of cells should be chosen accordingly, minimal voltage will maximize the current and vice versa! High voltage lines are expensive and difficult to justify in the economic aspect.
9) For this project since the battery pack and energy requirements are relatively lower than a typical passenger vehicle, we have chosen 30 cells in series. Parallel connections are tried to be avoided by most of the manufacturers. Avg voltage of a single cell is taken as 3.2V although it can vary from 2.6 -4.3V for minimum and maximum voltage respectively. 
10) Plot the results by importing all the data into the Matlab workspace. The time for the WLTP class 1 drive cycle is 1025 seconds. More information is given in the [MATLAB plot documentation](https://in.mathworks.com/help/matlab/ref/plot.html)
11) Interpret the data and understand how this data will provide valuable information for advanced heat dissipation calculations or motor selections.
  


   ![Current](https://github.com/jellyvisal/Predictive-battery-energy-requirements-/assets/142890460/f59ea082-b9da-4d02-b3bc-66807e799b0f)                     ![heat generated](https://github.com/jellyvisal/Predictive-battery-energy-requirements-/assets/142890460/cbae6bb4-baf5-4b72-b6d9-7cd8894bb19e)


We can observe that The maximum Heat generated is at the 769th second, where it is equal to 1kW of power lost in heat. 

## Conclusion 
In conclusion, the meticulous calculations and considerations related to energy battery capacity and heat dissipation requirements play a crucial role in designing efficient and reliable energy storage systems. By accurately assessing the energy demands of the intended application and factoring in variables such as discharge rates, operating temperatures, and heat generation, engineers can determine the optimal battery capacity and the necessary heat dissipation mechanisms.

In an era where sustainable energy solutions are paramount, these calculations not only ensure the reliable operation of energy storage systems but also pave the way for innovation and progress in various fields. Whether it's advancing electric vehicle technology, enabling the integration of renewable energy sources, or enhancing the resilience of power distribution networks, the data derived from energy battery calculations and heat dissipation requirements is the cornerstone upon which these advancements are built. As technology continues to evolve, the significance of accurate calculations and data-driven design approaches will only become more pronounced, driving us toward a greener and more energy-efficient future.



## Impact

Contribute to the electrification of transport worldwide. Provide data and increase the range, performance, and battery life of EVs.

## Skills attained 
MATLAB mscript, Microsoft Excel calculations, Vehicle dynamics, Energy Requirements, BCS requirements, Battery range optimizations 
