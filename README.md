Project Overview:
This project applies numerical methods to solve force balance equations for a cable-supported equipment housing weighing 1,500 kg. By modelling joint equilibrium as a system of linear algebraic equations (AX = B), we compute the specific tensions required in three high-tension cables to maintain static equilibrium in a 3D spatial environment.
Objectives:
•	Formulate equilibrium equations at the joints of a cable-supported structure.
•	Utilize unit vectors and direction cosines to decompose spatial forces across X, Y, and Z axes.
•	Implement and compare linear algebraic solvers in MATLAB, specifically the backslash operator () and matrix inversion.
Mathematical Model:
1. Static Equilibrium
For the structure to remain stationary, the sum of all internal and external forces acting on the suspension ring (Joint A) must be zero:
•	Horizontal Equilibrium: sum Fx = 0
•	Vertical Equilibrium: sum Fy = 0 and sum Fz = 0
2. Matrix Representation
The system is represented in the matrix form Kx = F, where:
•	K (Coefficient Matrix): Represents the geometric orientation (direction cosines) of the cables.
•	x (Unknown Vector): Represents the tensions (T1, T2, T3) at the joint.
•	F (Load Vector): Represents the external gravitational load (mg).
Problem Specifications:
The suspension ring is located at the origin (0, 0, 0) with cables anchored at the following coordinates:
•	Cable 1: (-4, 3, 10) 
•	Cable 2: (5, 4, 12) 
•	Cable 3: (0, -6, 8) 
Computational Solution:
MATLAB is utilized to solve the nonhomogeneous system efficiently.
•	Method: The Backslash Operator (\) is used as the primary solver due to its numerical efficiency for multi-dimensional problems.
•	Alternative: Matrix Inversion (inv) is available but noted as less efficient for larger systems.
