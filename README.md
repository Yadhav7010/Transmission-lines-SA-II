## **Field Equations in Rectangular Waveguide**

---

### **1. Aim**

To derive and study the **field equations** governing electromagnetic wave propagation in a **rectangular waveguide**, and to understand how the electric and magnetic fields behave for different modes (TE and TM).

<img width="300" height="168" alt="image" src="https://github.com/user-attachments/assets/9b8ac329-f597-45fb-8459-4fb946e81c34" />

---

### **2. Apparatus / Requirements**

* Knowledge of **Maxwell’s equations** in phasor form
* Basic understanding of **boundary conditions** for conductors and dielectrics
* Geometry of a **rectangular waveguide** (dimensions ( a ) × ( b ))
* Mathematical tools for partial differential equations
* <img width="653" height="414" alt="image" src="https://github.com/user-attachments/assets/9bcaa5ca-c692-411f-a2f9-c229bfd93850" />


---

### **3. Theory**

#### **a) Introduction**

A **waveguide** is a hollow metallic structure that guides electromagnetic waves from one point to another.
The **rectangular waveguide** is one of the simplest and most widely used types in microwave and radar systems.
It supports electromagnetic waves above a certain **cutoff frequency**, allowing efficient transmission with minimal loss.
<img width="433" height="241" alt="image" src="https://github.com/user-attachments/assets/b0e5ab0c-76bc-459a-abd5-e99f535624f6" />


---

#### **b) Geometry**

Consider a rectangular waveguide of dimensions:
[
a = \text{width (along x-axis)}, \quad b = \text{height (along y-axis)}
]
and the wave propagates in the **z-direction**.
<img width="504" height="375" alt="image" src="https://github.com/user-attachments/assets/ecd729cf-8ce1-491a-9f36-92862e24fff1" />


---

#### **c) Maxwell’s Equations (in Phasor Form)**

[
\nabla \times \mathbf{E} = -j\omega \mu \mathbf{H}
]
[
\nabla \times \mathbf{H} = j\omega \epsilon \mathbf{E}
]
[
\nabla \cdot \mathbf{E} = 0
]
[
\nabla \cdot \mathbf{H} = 0
]

These equations describe how electric (( \mathbf{E} )) and magnetic (( \mathbf{H} )) fields are related and vary in space and time.
<img width="1024" height="791" alt="image" src="https://github.com/user-attachments/assets/7fe57466-5e5e-459d-8b2f-6c2ccd443ab7" />


---


#### **d) Wave Equation for Fields**

Applying the curl operator to Maxwell’s equations leads to the **vector wave equations**:
[
\nabla^2 \mathbf{E} + k^2 \mathbf{E} = 0
]
[
\nabla^2 \mathbf{H} + k^2 \mathbf{H} = 0
]
where ( k = \omega \sqrt{\mu\epsilon} ) is the **wave number** in the medium.
<img width="501" height="441" alt="image" src="https://github.com/user-attachments/assets/631fa726-64dc-4df0-b92a-a272c518d5d8" />


---

#### **e) Field Components**

The electromagnetic fields inside the waveguide can be expressed in terms of **transverse (x, y)** and **longitudinal (z)** components:
[
\mathbf{E} = \mathbf{E}_t + \hat{z}E_z, \quad \mathbf{H} = \mathbf{H}_t + \hat{z}H_z
]

Depending on whether ( E_z ) or ( H_z ) is zero, we have two types of modes:

* **TE (Transverse Electric) Mode:** ( E_z = 0 ), ( H_z \neq 0 )
* **TM (Transverse Magnetic) Mode:** ( H_z = 0 ), ( E_z \neq 0 )
* <img width="582" height="330" alt="image" src="https://github.com/user-attachments/assets/e4828fc3-fc86-4660-abb8-4a6432def0b3" />


---

### **4. Field Equations for TE Modes**

For **TE modes**, since ( E_z = 0 ), we derive from Maxwell’s equations:

[
\nabla_t^2 H_z + (k^2 - \beta^2)H_z = 0
]

The solution for ( H_z ) inside the rectangular waveguide is:
[
H_z(x, y) = H_0 \cos\left(\frac{m\pi x}{a}\right)\cos\left(\frac{n\pi y}{b}\right)
]
where

* ( m, n ) are integers representing mode numbers,
* ( \beta ) is the **phase constant** along z-direction.

The corresponding transverse components are obtained using:
[
E_x = \frac{j\omega\mu}{k_c^2} \frac{\partial H_z}{\partial y}, \quad
E_y = -\frac{j\omega\mu}{k_c^2} \frac{\partial H_z}{\partial x}
]
[
H_x = -\frac{j\beta}{k_c^2} \frac{\partial H_z}{\partial x}, \quad
H_y = -\frac{j\beta}{k_c^2} \frac{\partial H_z}{\partial y}
]
where ( k_c^2 = \left(\frac{m\pi}{a}\right)^2 + \left(\frac{n\pi}{b}\right)^2 ) is the **cutoff wavenumber**.
<img width="1223" height="2560" alt="image" src="https://github.com/user-attachments/assets/54a72f28-44b8-434c-82fd-10a9ebe109cc" />


---

### **5. Field Equations for TM Modes**

For **TM modes**, since ( H_z = 0 ), we have:
[
\nabla_t^2 E_z + (k^2 - \beta^2)E_z = 0
]

The general solution is:
[
E_z(x, y) = E_0 \sin\left(\frac{m\pi x}{a}\right)\sin\left(\frac{n\pi y}{b}\right)
]

The corresponding transverse field components are:
[
H_x = \frac{j\omega\epsilon}{k_c^2} \frac{\partial E_z}{\partial y}, \quad
H_y = -\frac{j\omega\epsilon}{k_c^2} \frac{\partial E_z}{\partial x}
]
[
E_x = -\frac{j\beta}{k_c^2} \frac{\partial E_z}{\partial x}, \quad
E_y = -\frac{j\beta}{k_c^2} \frac{\partial E_z}{\partial y}
]
<img width="501" height="441" alt="image" src="https://github.com/user-attachments/assets/e58887de-48a0-4873-b431-9f11b62da4b1" />


---

### **6. Cutoff Frequency**

For a given mode ( (m, n) ):
[
f_c = \frac{1}{2\pi\sqrt{\mu\epsilon}} \sqrt{\left(\frac{m\pi}{a}\right)^2 + \left(\frac{n\pi}{b}\right)^2}
]

Only frequencies **above ( f_c )** will propagate through the waveguide.
The dominant mode (lowest ( f_c )) in rectangular waveguides is **TE₁₀**.

<img width="1320" height="505" alt="image" src="https://github.com/user-attachments/assets/e3938ab4-9d85-42b2-be0d-036901f074a8" />

---

### **7. Applications**

* Used in **microwave transmitters and radar systems**.
* Employed for **satellite communication** and **radar antennas**.
* Provides **low loss and high power handling** compared to coaxial cables.
* Forms the basis for **microwave filters, oscillators, and couplers**.
* <img width="663" height="378" alt="image" src="https://github.com/user-attachments/assets/0f726157-ae85-4dff-98de-ca077c357549" />


---

### **8. Conclusion**

Rectangular waveguides guide electromagnetic energy efficiently by confining electric and magnetic fields within a hollow metallic structure.
By applying Maxwell’s equations, the field components and propagation characteristics for **TE and TM modes** can be derived.
Understanding these field equations helps engineers design **microwave communication systems**, **radar components**, and **high-frequency transmission networks** with optimal performance and minimal loss.

<img width="275" height="183" alt="image" src="https://github.com/user-attachments/assets/211158eb-1e96-40e4-a116-c43fcc3ed236" />


---
