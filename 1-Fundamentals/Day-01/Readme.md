# Day 1 : Charge , Electric field and Potential Diffrence

---

## what do we mean by electric charge ?

matter is made of atoms. every atom a nucleus (protons and neutrons) surrounded by electrons in orbit shells 
protons carries a positive charge and electrons carries negative charge of equal magnitude.

atomes are classified based on their electric charge and there are mainly two types :
- neutral atom : when number of protons = number of electrons for example a 'H' atom (hydrogen atom)
- Ion (charged atom) : when an atom gain or loses one or more electrons there is two types of Ions
    - cation (positive ion) : loses electrons (num protons > num electrons) exmaple : Na+ (Sodium ion)
    - anion (negative ion) : gain electrons (num protons < num electrons) example : Cl- (Chloride anion)

There are two kinds of electric charge, positive and negative. On the atomic level, protons are positively charged and electrons are negatively charged.
in a neutral atom the net charge is zero because the num electrons = num protons
the electric charge carried by a single proton, quantified as 1.602176634 × 10^-19 coulombs.
the electric charge carried by a single electron is -1.602176634 × 10^-19 coulombs (negative of the proton's charge).

---

## What is a Coulomb?

The **coulomb (C)** is the SI unit of electric charge. 
One coulomb = charge transferred by 1 ampere of current in 1 second.
One coulomb ≈ charge of 6.242 × 10¹⁸ protons (or electrons).
It's the standard unit used to measure electric charge in electrical circuits and physics.

in electronics we rarely deal with whole coulombs, instead we use smaller units like microcoulombs (µC) or nanocoulombs (nC) to express the charge of particles or small objects.
- 1 microcoulomb (µC) = 10^-6 coulombs
- 1 nanocoulomb (nC) = 10^-9 coulombs

---

now lets talk about conductors and insulators
- **Conductors** are materials that allow electric charge to flow freely through them. They have low resistance and are typically made of metals like copper, aluminum, and silver. In conductors, electrons can move easily, making them good for transmitting electricity.
- **Insulators** are materials that do not allow electric charge to flow freely. They have high resistance and are typically made of non-metallic materials like rubber, glass, and plastic. In insulators, electrons are tightly bound to their atoms and cannot move freely, making them good for preventing the flow of electricity.
- **Semiconductors** are materials that have electrical conductivity between that of conductors and insulators. They can be made to conduct electricity under certain conditions, such as when exposed to light or heat. Common semiconductor materials include silicon and germanium, which are widely used in electronic devices like transistors and diodes.

---

# Coulomb's Law
two point charges exert a force on each other. this relationshio is described by charles-augustin de coulomb in 1785 and is known as Coulomb's law.
coulomb's law describes the force between two charged objects. The formula is:
F = k * (|q1 * q2| / r^2)

Where:
- F is the force between the charges in newtons (N)
- k is Coulomb's constant (approximately 8.988 × 10^9 N⋅m²/C²)
- q1 and q2 are the magnitudes of the charges in coulombs (C)
- r is the distance between the charges in meters (m)

coulomb's constant (k) also can be written as:
k = 1 / (4 * π * ε₀)

Where:
- ε₀ is the permittivity of free space (8.85418782 × 10^-12 F/m)
the force (F) is attractive if the charges have opposite signs (one positive and one negative) and repulsive if the charges have the same sign (both positive or both negative).

Why does this matter for embedded systems? 

Think of everything in electronics as tiny invisible forces between charges, described by Coulomb's Law. 
A **capacitor** is like two rooms separated by a wall: you pack one room with positive charges and the other with negative ones. They strongly want to reunite, and that “tension” between them is stored energy. 
The wall (dielectric : عازل) is not perfectly solid, so a few charges slowly sneak through it this is leakage, helped by effects like Quantum Tunneling.

A **Metal-Oxide-Semiconductor Field-Effect Transistor (MOSFET)** works in a similar way but uses influence instead of direct contact. Imagine a glass wall with a metal plate on top (the gate). When you add charge to the gate, it creates an electric field that pulls charges into a path below it, like organizing people into a line without touching them. That’s how current starts flowing. But to create that field, you first need to “fill” the gate with charge, just like filling a small bucket—this is the gate charge.

Finally, you cannot instantly change the voltage across a capacitor because that would mean instantly moving a huge number of charges from one side to the other. In reality, moving charge is like moving a crowd through a doorway—it takes time because the flow (current) is limited. So voltage always changes gradually, not instantly.

---
# Electric Field

The electric field E at a point in space is defined as the force per unit positive charge that would be experienced by a test charge placed at that point. Mathematically, it can be expressed as:
E = F / q

Where: 
- E is the electric field in newtons per coulomb (N/C)
- F is the force in newtons (N)
- q is the test charge in coulombs (C)
The electric field is a vector quantity, meaning it has both magnitude and direction. The direction of the electric field is defined as the direction of the force that a positive test charge would experience.
The electric field due to a point charge can be calculated using Coulomb's law:
E = k * (|q| / r^2)
Where:
- E is the electric field in newtons per coulomb (N/C)
- k is Coulomb's constant (approximately 8.988 × 10^9 N⋅m²/C²)
- q is the point charge in coulombs (C)
- r is the distance from the point charge in meters (m)

The electric field is a vector - it has both magnitude and direction. 
Field lines point from positive charges toward negative charges

Electric field between parallel plates is the geometry (هندسة) of every capacitor:
E = V / d
Where V is the voltage across the plates and d is the separation distance. This is one of the most important formulas in electronics - it tells you the stress the dielectric is under. If you exceed the breakdown field of the dielectric
material (typically 10-100 MV/m for common materials), you will permanently
damage the capacitor.

| Material | Breakdown Field (MV/m) |
|----------|------------------------|
| Air | ~3 |
| Silicon Dioxide (SiO₂) | ~10 |
| Polyimide | ~200 |
| FR4 PCB Material | ~20 |
| Ceramic | ~100 |

that's why we need to be careful when designing circuits with high voltages or small distances between conductors, as it can lead to dielectric breakdown and damage to components.

that's all for today, i will study more about electric potential difference and how it relates to electric field tomorrow. see you then :) 

**p6**