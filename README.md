# experiment1
## **aim** 
obtain the DC analysis,transient and AC analysis of the CS amplifier to obtain various parameters using LT spice.
## **required components**
MOSFET(nmos4),resistor (1k),voltage (1.8v,0.9v),connecting wires
## **circuit diagram**
![Screenshot (13)](https://github.com/user-attachments/assets/d174a185-b8e6-43b4-bf21-7275bf3a8bf1)

## **theory**
mosfet is a type of transister widely used in digital and analog circuits.it operates as voltage controlled device, allowing current to flow between its drain and source terminal based on the voltage applied on gate terminal.the working principle of the mosfet is when voltage is applied to the gate terminal electric field is created influcing the charge carriers in the channel region . there are 3 modes of operation  that is cutoff region,triode region and saturation region.in the cutoff region the voltage acoss gate and source is less than the threshold so no current flows,in thriode when the voltage across gate and source is less than threshold allows current to flow with low resistance'in saturation region the voltage across gate and souce is greater than the threshold so maxium current flows in this region.
## **parameters**
length: 180nm
vDD(v1): 1.8v
vGS(v2): 0.9v
resistance value: 1k
## **procedure**
design the CS amplifier as per the given parameters using the LT spice
now give the values to the components used in the parameter that is (resistor 1k,VDD 1.8V,VGS 0.9v)
create a new folder and save the lt spice file in the folder with the library file
find the current value for the given power rating that is(100uw)
now give the different values for length and width 
## **DC analysis** 
by varing the length and width go to the configure analysis and select DC analysis , run the simulations we obtain the simulations as shown in the figure.(.op)
this helps in determining the DC operating point
![Screenshot (17)](https://github.com/user-attachments/assets/cf2751b5-bfa6-4732-ab74-ef4a8a393240)

**tabular column**
<table>
<tr>
   <td>length></td>
   <td>width</td>
   <td>I<sub>d</sub></td>
</tr> 
  <tr>
  <td>180nm</td>
  <td>0.2u</td>
  <td>55.2uA</td>
</tr>
  <td>180nm</td>
  <td>0.203um</td>
  <td>55.5uA</td>
</tr>
    <tr>
  <td>180nm</td>
  <td>1um</td>
  <td>4.5</td>
</tr>
</table>

**transient analaysis**
apply the sine wave input of frequency 1KHz and amplitude 50mV
go to the simulate configure and select the transient analysis option(.trans 5ms)
give the stop time as 5ms and then run the simulations
![image](https://github.com/user-attachments/assets/20cd34f2-f189-4c71-8945-b18d83adde06)


**AC analysis**
go to the simulate option in the tab,edit the simulation command
click the AC analysis and give the time as decade,number of points as 20,freuency as 1Hz to 1THz and click on okay
now run the analysis the gain and frequency response is obtained
![image](https://github.com/user-attachments/assets/32a14381-e0ed-4363-af39-317a68b5072c)


 **caculations**<br>
 power is 100uW<br>
 VDD is 1.8v<br>
 I<sub>d</sub> is 100u/1.8<br>
 =55.5uA
 from the loop equation VDD=I<sub>d</sub>+vout<br>
 therefore,vout=1.745v<br>
 hence the q point is (vout,i<sub>d</sub>)<br>
 =(1.745v,55.5uA)

 **result**
 DC analysis Id= 55.5uA
 for width of 6.85um and length of 1um<br> and vout id 1.745v
<br> therefore operating point is (1.745v,55.5uA)<br>
![Screenshot (17)](https://github.com/user-attachments/assets/c8d8480a-5db0-46ec-8f67-fd8d32d788db)



**transient analysis**
vout = .543V<br>
There is 180 degree phase shift between iput and output<br>

![WhatsApp Image 2025-02-16 at 23 08 03_a9d53844](https://github.com/user-attachments/assets/455d3620-04fc-4d8d-b563-f66573c04699)


**AC analysis**
gain is -9.10dB
![WhatsApp Image 2025-02-16 at 23 06 45_7ac9acae](https://github.com/user-attachments/assets/7bb14577-27fb-4c0e-aa64-8874f94900ec)


**inference**
the circuit is designed for 1k drain resistor<br>.it is providing voltage gain with inverted output.<br> AC gain helps us to obtain the frequency response and gain.<br>however proper biasing is crutial for for the transistor to operate in saturation region the mosfet gain is increasedin the mid band frequencyrange that is small signal analysis<br> we also observe that the current varies with respect to that of the width.

##circut_2
## **aim** 
obtain the DC analysis,transient and AC analysis of the CS amplifier to obtain various parameters using LT spice.
## **required components**
MOSFET(nmos4),(pmos4),voltage (1.8v,0.7v),connecting wires
## **circuit diagram**
![Screenshot (20)](https://github.com/user-attachments/assets/1380ac15-b5a3-46a2-a4a8-555559b4e08c)
## **theory**
mosfet is a type of transister widely used in digital and analog circuits.it operates as voltage controlled device, allowing current to flow between its drain and source terminal based on the voltage applied on gate terminal.the working principle of the mosfet is when voltage is applied to the gate terminal electric field is created influcing the charge carriers in the channel region . there are 3 modes of operation  that is cutoff region,triode region and saturation region.in the cutoff region the voltage acoss gate and source is less than the threshold so no current flows,in thriode when the voltage across gate and source is less than threshold allows current to flow with low resistance'in saturation region the voltage across gate and souce is greater than the threshold so maxium current flows in this region.
## **procedure**
design the CS amplifier as per the given parameters using the LT spice
now give the values to the components used in the parameter 
create a new folder and save the lt spice file in the folder with the library file
find the current value for the given power rating that is(100uw)
now give the different values for length and width by trail and error method for nmos and pmos to get respective drain current 
## **DC analysis** 
by varing the length and width go to the configure analysis and select DC analysis , run the simulations we obtain the simulations as shown in the figure.(.op)
this helps in determining the DC operating point
![Screenshot (22)](https://github.com/user-attachments/assets/7f76d4f2-8526-43db-80eb-0edd87dc3e2e)

**tabular column**
<table>
<tr>
   <td>length></td>
   <td>width</td>
   <td>I<sub>d</sub></td>
</tr> 
  <tr>
  <td>180nm</td>
  <td>5.86um</td>
  <td>40.83uA</td>
</tr>
  <td>180nm</td>
  <td>2.55u</td>
  <td>69.46uA</td>
</tr> 
   <tr>
   <td>180nm</td>
   <td>2.02</td>
   <td>54.98uA></td>
</tr> 
</table>

**transient analaysis**
apply the sine wave input of frequency 1KHz and amplitude 50mV
go to the simulate configure and select the transient analysis option(.trans 5ms)
give the stop time as 5ms and then run the simulations
![Screenshot (24)](https://github.com/user-attachments/assets/4cd1d3dd-18a2-48d5-8109-17366f4c6d0f)


**AC analysis**
go to the simulate option in the tab,edit the simulation command
click the AC analysis and give the time as decade,number of points as 20,freuency as 1Hz to 1THz and click on okay
now run the analysis the gain and frequency response is obtained
![WhatsApp Image 2025-02-17 at 23 22 25_941c5154](https://github.com/user-attachments/assets/5403d8a1-d3a7-418a-a74e-db674c460a80)
**calculations**
take power as 100uW<br>.
P=V*I where v is 1.8V<br>.
therefore I=54.98uA<br>.
we get Vout as 1.658<br>.
Qpoint is(1.658v,54.98uA)



 **result**
 DC analysis Id= 54.98uA<br>
 for width of 1.02um and length of 180nm<br> and vout  1.658v
<br> therefore operating point is (1.658v,54.98uA)<br>
![Screenshot (22)](https://github.com/user-attachments/assets/223071b9-71f6-4b7f-9c46-706a8f49877a)
**transient analysis**<br>
There is 180 degree phase shift
![Screenshot (24)](https://github.com/user-attachments/assets/4cd1d3dd-18a2-48d5-8109-17366f4c6d0f)
**AC anlysis**<br>
gain is 3.8dB
![WhatsApp Image 2025-02-17 at 23 22 25_941c5154](https://github.com/user-attachments/assets/5403d8a1-d3a7-418a-a74e-db674c460a80)

 **inference**
 **DC analysis**
 the data shows the effect of the varing transistor width on current and the output voltage<br>
 as the width decreases the current also decreases that is directly propotional<br>
 the output voltage increases as the drain current decreases(inverse relationship)<br>
 **transient analysis**
 it gives the study of voutput and drain current respond to time varying input signal
 in the transient rise time,fall time is analysied that is the circuits response time
 due to the variation of the in capacitance and current flow<br>
 **AC analysis**
 AC analysis examins the small signal behavior of the circuit<br>
 the gain and the frequency response is determined by analysisthe width variation on small signal parameters


 


 
 








 
 
 






   
  
   








