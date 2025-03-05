# the mos differential pair amplifier<br>
 differential amplifier pair amplifier is the circuit that ampifies the difference between two input signal while rejecting the common mode noise.The circuit consists of two MOSFETs that amplify the difference between two input signals while rejecting common-mode noise. Essentially, a differential amplifier combines inverting and non-inverting amplifiers. <br>
this mos has main application in operational amp,analog to digital convertors,sensor interface etc <br>
this amplifier has high input impedence:good for interfacing with other high impedence sources <br>
provides accurate signal amplification <br>
## schematc diagram of mos differential amplifier
### there are 4 types of differential amplifier<br>
### Resistor-Loaded Differential Pair:<br>
*Uses resistors as the drain load.<br>
*Simple design but has low gain due to large requirements.
*Limited common-mode rejection and output swing.

### Current Source-Loaded Differential Pair:<br>
Replaces Rss with Ideal current source.<br>
Improves gain.<br>
### Simple Current Source Differential Pair:<br>
Uses a single MOSFET as a current source.<br>
Gain increases still.<br>
### Active Load Differential Pair (MOSFET as Load):<br>
Both Iss and Rd are replaced with a mosfet .<br>
Gain is too high.<br>
### working principle<br>
the differential amplifier operates in the active region and can function in different modes: common-mode and differential-mode .<br>
the differential amplifier has 2 input terminals that is V1 and V2 (non inverting and inverting)<br>
'the output is determined by difference between 2 inputs <br>
Common-Mode Rejection:
If both input signals are identical (common-mode signals), the ideal differential amplifier cancels them out, giving zero output.
This property is measured by the Common-Mode Rejection Ratio (CMRR).
It receives two input signals and compares them.<br>
It amplifies only the difference between the two inputs.<br>
Any noise or interference present in both inputs is removed.<br>
The output changes based on the difference between the input signals.<br>
Feedback is often used to stabilize gain and improve <br>
### key features
High Common-Mode Rejection Ratio (CMRR): Rejects noise present in both inputs.<br>
Good Stability: Less sensitive to variations in power supply or temperature.<br>
Used in Instrumentation Amplifiers: Provides precise low-noise amplification.<br>
Forms the Basis of Op-Amp Circuits: Essential in signal processing.<br>
## aim of the experiment: design and analyze the mos differntial amplifier circuit for following specifications<br>
VDD=1.8v,P=1.8mW,Vin=0.9v,Vocm=0.9v,Vp=0.2V<br>
### components required:
RSS->stabilizes biasing which further provides negative feedback<br>
RD->this is the drain resistance converts currend into o/p voltage<br>
id->drain current(ensure the transistor is in saturation region)<br>
iss-> tail current( provides stable constant current)<br>
#### note :
the output can be either differential orsingle ended,if the v_1=v_2 then the outpu voltage will be 0V<br>
### calculations of the desing part:
### from LT spice we observe that
as the VDD increases ,vout also increases and more is the gain<br>
when width increases curret flowing also increases but vout decreases,gain is more<br>
as RD increases vout also increases gain increases<br>
when RSS increases gain get reduced but common mode rejection is bettered<br>
### case 1(resistor loaded differential pair)
#### DC Analysis :
Make the necessary connections as per the circuit daigram .<br>
Set the Rd and Rss values such that the transistors will operate in saturation region .<br>
Vary W/L to get the required Voutcm.<br>
Vary Rd to set exact Voutcm.<br>
Go to "Simulate" > "Edit Simulation Cmd" > "DC op pnt".<br>
ckt1 dc<br>
### specification values and observed values 
 <table>
 <tr>
   <td>parameter</td>
   <td>specification values</td>
  <td>observed values</td>
 </tr>
 <tr>
   <td>vout</td>
   <td>specification values</td>
  <td>observed values</td>
 </tr>
<tr>
   <td>Vp</td>
   <td>specification values</td>
  <td>observed values</td>
 </tr>
<tr>
   <td>Id1,Id2</td>
   <td>specification values</td>
  <td>observed values</td>
 </tr>
<tr>
   <td>RD</td>
   <td>specification values</td>
  <td>observed values</td>
 </tr>
<tr>
   <td>RSS</td>
   <td>specification values</td>
  <td>observed values</td>
 </tr>
<tr>
   <td>Vgs</td>
   <td>specification values</td>
  <td>observed values</td>
 </tr>
<tr>
 <br>
 
 ### transient analysis:<br>
 Replace DC input with an AC signal.<br>
Use SINE(dc_offset, Amplitude, Frequency)..<br>
Go to "Simulate" > "Edit Simulation Cmd" > "Transient"..<br>
Set Stop Time: 5ms..<br>
Run the simulation.
### AC analysis:



  











