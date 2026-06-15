# 05-DESIGN-AND-ANALYSIS-OF-MICROSTRIP-ANTENNA-USING-CST-MICROWAVE-STUDIO (LAYOUT)

**Aim of the Experiment:** To design a quarter wave transformer for matching a 50 Ohm microstrip line with a load of 123 Ohms
Software to be used: CST studio suite 2019 (Student edition)

**Design:**

**Mathematical Calculation**

<img width="601" height="420" alt="image" src="https://github.com/user-attachments/assets/b6c74464-e862-4d26-be7c-e76738107067" />

Width of the quarter wave line=1.138 mmWidth of the stripline=2.93 mm
Height of the substrate=1.6 mmZ0=50 ohm,ZL=123 ohm Zo’=√(50*123)= 78.42 ohm
Length of the quarter wave line = 18mmLamda g =72 , Lamda not=128
Bandwidth calculation from s-parameter in quater wave line=1.33 GhzFrequency=2.4 Ghzc, Ε eff=3.024

# Procedure
# Design and Analysis of Microstrip Patch Antenna Using CST Microwave Studio (Layout)

## Aim

To design and analyze a rectangular microstrip patch antenna using CST Microwave Studio and obtain its characteristics such as resonant frequency, return loss, VSWR, gain, and radiation pattern.

---

# Simple Procedure

## Step 1: Open CST Microwave Studio

1. Launch **CST Microwave Studio**.
2. Click **New Project**.
3. Select **Microwave & RF** → **Antenna**.
4. Choose **Time Domain Solver** (or Frequency Domain Solver).
5. Click **OK**.

---

## Step 2: Set Units

1. Go to **Modeling → Units**.
2. Set:

   * Length = **mm**
   * Frequency = **GHz**
   * Time = **ns**
3. Click **OK**.

---

## Step 3: Define Antenna Parameters

Enter the dimensions of the antenna.

Example:

| Parameter             | Value  |
| --------------------- | ------ |
| Substrate Length (Ls) | 60 mm  |
| Substrate Width (Ws)  | 50 mm  |
| Substrate Height (h)  | 1.6 mm |
| Patch Length (Lp)     | 29 mm  |
| Patch Width (Wp)      | 38 mm  |
| Feed Width (Wf)       | 3 mm   |
| Feed Length (Lf)      | 15 mm  |

*(Values may vary according to the desired frequency.)*

---

## Step 4: Create the Substrate

1. Click **Modeling → Brick**.
2. Draw a rectangular block.
3. Enter substrate dimensions:

   * Length = 60 mm
   * Width = 50 mm
   * Height = 1.6 mm
4. Assign material as **FR4**.

This forms the dielectric substrate.

---

## Step 5: Create Ground Plane

1. Draw a metallic sheet below the substrate.
2. Use the same length and width as the substrate.
3. Thickness can be very small (e.g., 0.035 mm).
4. Assign material as **Copper (PEC)**.

This acts as the ground plane.

---

## Step 6: Create the Patch

1. Draw a rectangular sheet on the top surface of the substrate.
2. Set dimensions:

   * Length = 29 mm
   * Width = 38 mm
3. Assign material as **Copper**.

This is the radiating patch.

---

## Step 7: Create the Feed Line

1. Draw a microstrip feed line connected to the patch.
2. Set dimensions:

   * Width = 3 mm
   * Length = 15 mm
3. Assign Copper material.

The feed line supplies power to the antenna.

---

## Step 8: Add Port

1. Select **Simulation → Discrete Port** or **Waveguide Port**.
2. Place the port at the end of the feed line.
3. Set impedance as **50 Ω**.

This provides excitation to the antenna.

---

## Step 9: Set Boundary Conditions

1. Go to **Simulation → Boundary Conditions**.
2. Select **Open (Add Space)** for all sides.
3. Click **OK**.

This allows the antenna to radiate freely.

---

## Step 10: Set Frequency Range

1. Click **Simulation → Frequency Range**.
2. Enter:

   * Start Frequency = 1 GHz
   * Stop Frequency = 5 GHz

(Choose the range according to the antenna design.)

---

## Step 11: Mesh Generation

1. Click **Mesh → Global Mesh Properties**.
2. Keep default settings or select automatic mesh.
3. Generate mesh.

The mesh divides the antenna into small cells for analysis.

---

## Step 12: Run Simulation

1. Click **Start Simulation**.
2. Wait until the solver completes the analysis.

---

# Analysis of Results

## 1. Return Loss (S11)

1. Open **Results → S-Parameters**.
2. Observe the S11 graph.

### Interpretation

* Resonance occurs where S11 is minimum.
* Good antenna:

  * S11 < -10 dB

Example:

| Frequency | S11    |
| --------- | ------ |
| 2.45 GHz  | -25 dB |

---

## 2. VSWR

1. Open **Results → VSWR**.

### Interpretation

| VSWR | Performance |
| ---- | ----------- |
| 1    | Perfect     |
| < 2  | Good        |
| > 2  | Poor        |

Example:

VSWR = 1.2

---

## 3. Gain

1. Open **Farfield Results → Gain**.
2. Note the maximum gain.

Example:

Gain = 6 dBi

---

## 4. Radiation Pattern

1. Open **Farfield Pattern**.
2. Observe:

   * Main lobe
   * Side lobes
   * Beam direction

This shows how the antenna radiates energy.

---



**	Design of microstrip line terminated with the desired load**


<img width="621" height="185" alt="image" src="https://github.com/user-attachments/assets/908adc01-814f-450c-b969-7e1342681af4" />


**S11 characteristics of the microstrip line terminated with the load**


<img width="640" height="203" alt="image" src="https://github.com/user-attachments/assets/f7d30519-56c3-4642-b446-7b93a7a1e33b" />


**	Design of microstrip line terminated with quarter wave line and the desired load**


<img width="642" height="184" alt="image" src="https://github.com/user-attachments/assets/4fcf36a6-131b-45e0-b569-8f50565faf0e" />


**	S11 characteristics of the microstrip line terminated with quarter wave line and the desired load**


<img width="558" height="162" alt="image" src="https://github.com/user-attachments/assets/863dbdd2-254c-4165-b167-3bdbb331efc7" />



**Design**


<img width="732" height="327" alt="image" src="https://github.com/user-attachments/assets/5ee28470-864c-4433-80c5-880f3cf09aba" />

<img width="762" height="348" alt="image" src="https://github.com/user-attachments/assets/d4806f51-79d0-435a-b7e0-bcc056fcce78" />


<img width="863" height="412" alt="image" src="https://github.com/user-attachments/assets/2432011a-a4f7-4671-9f2a-7723787ee70e" />



**Output**


<img width="801" height="407" alt="image" src="https://github.com/user-attachments/assets/22d1c084-98ad-4363-a758-fead927f1669" />

**Conclusion:**

From this experiment we got the bandwidth value of 1.33 Ghz with a impedance matching of 78.42 ohm and also got the width of quarter wave line of 1.138 mm.




