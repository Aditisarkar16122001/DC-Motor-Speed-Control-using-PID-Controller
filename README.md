# DC-Motor-Speed-Control-using-PID-Controller
# DC Motor Speed Control using PID Controller (MATLAB + Simulink)

## Project Overview
This project demonstrates **DC motor speed control** using a **PID (Proportional–Integral–Derivative) controller**. The system is modeled and analyzed in **MATLAB** and **Simulink**, comparing performance **with and without PID control**.

The objective is to improve system performance in terms of:
- Rise time  
- Settling time  
- Overshoot  
- Stability  

---

##  System Model

The DC motor is modeled using the transfer function:

$G(s) = \frac{ 1 }{s² + 10s + 20}$

---

##  MATLAB Implementation

###  Open Loop Analysis (Without PID)
- Step Response
  ![without PID](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/without%20PID%20MATLAB.png)
- Pole-Zero Map
  ![OL Pole Zero (without PID)](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/Open%20Loop%20Pole%20Zero(without%20PID).png)
  Open Loop Poles:
   -7.2361 ,
   -2.7639
- Root Locus
 ![without PID](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/Root%20Locus%20plot%20(without%20PID).png)
- Bode Plot
   ![without PID](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/Bode%20Plot(without%20PID).png)

###  PID Controller Parameters
Kp = 200  
Ki = 150  
Kd = 30  

Controller:
$C(s) = Kp + \frac{Ki}{s} + K_{d}s$

###  Closed Loop System
$T(s) = \frac{C(s)G(s)}{1 + C(s)G(s)}$

###  Performance Evaluation
- Step Response Comparison
  ![comparison](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/without%20PID%20vs%20with%20PID.png)
- Stability Analysis  
- Gain & Phase Margins  
- Step Response Metrics 

---

##  Simulink Model

###  Without PID
- Step Input → DC Motor → Feedback Loop  
- Basic closed-loop system without controller  
![Simulink without PID](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/Without%20PID.png)

###  With PID Controller
- Step Input → PID Controller → DC Motor → Feedback  
- PID improves system response significantly  
![Simulink with PID](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/With%20PID.png)

###  PID Parameters Used
- Proportional Gain (P): 200  
- Integral Gain (I): 150  
- Derivative Gain (D): 30  
![PID Parameters](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/KP%2CKI%2CKD%20Values.png)
---

##  Results & Observations

###  Without PID:
![without PID](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/Response%20Without%20PID.png)
- Slower response  
- Larger steady-state error  
- Less control over dynamics  

###  With PID:
![With PID](https://github.com/Aditisarkar16122001/DC-Motor-Speed-Control-using-PID-Controller/blob/main/Response%20With%20PID.png)
- Faster rise time  
- Reduced steady-state error  
- Improved stability  
- Better transient response  

---

##  Key Plots Generated
- Step Response (Open Loop vs Closed Loop)  
- Pole-Zero Map  
- Root Locus  
- Bode Plot  
- Gain & Phase Margins  

---

##  Tools Used
- MATLAB  
- Simulink  
- Control System Toolbox  

---

  
