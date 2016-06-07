Board Description
-----------------

board designation           : SoDeRa-PCIe
board version		        : v1.0
board type                  : Lead Free
board size                  : 136.85 mm x 68.9 mm
board thickness             : 1.6 mm +/- 10 %
board material              : IT-180A
number of layers            : 12 (10 inner)
 

Top layer copper foil thickness: 17.5 um
Dielectric thickness between Top layer and 2nd layer: 173 um (6.8 mils)
Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2

Bottom layer copper foil thickness: 17.5 um
Dielectric thickness between L11 layer and Bottom layer: 173 um (6.8 mils)
Dielectric between L11 and Bottom layer relative permittivity (Er): 4.2

Internal layer copper foil thickness: 33um

minimum finished hole size  :  200 um
minimum spacing             :  100 um
minimum track width         :  100 um

drill diameters             : finished hole

plating finish (both sides) : immersion gold
                              0.05-0.10 um of gold over
                              2.50-5.00 um of nickel

plating finish PCI fingers (both sides) : immersion gold
                              30 micro inches of gold over
                              50 micro inches of nickel
							  
PCB edges below PCI express fingers must be chamfered. Chamfer height 1.4 mm, angle 20 (+/-5) degrees. Edges must be free of cutting burrs. Details given on PCB.
							  
Top silkscreen              : Required
Bottom silkscreen           : Required

Drill files
-----------------
   - SoDeRa-PCIe_1v0.DRR -> Drill report detailing the tool assignments, hole sizes, hole count and tool travel. 
   
   - Throughole vias are covered in the following files:
   								File Name																	Start Layer						Stop Layer
						SoDeRa-PCIe_1v0-RoundHoles.TXT															Top									Bottom
   - Slotholes are covered in the following files:
						SoDeRa-PCIe_1v0-SlotHoles.TXT															Top									Bottom	
						
	- IMPORTANT! Hole diameters are final manufactured diameters INCLUDING HOLE METALIZATION.
	
Gerber files
---------------

			File Name					Layer/Comment
		SoDeRa-PCIe_1v0.GTL				Top (RF/GND)
		SoDeRa-PCIe_1v0.G1				L2  (GND)
		SoDeRa-PCIe_1v0.G2				L3  (PWR/Siglan/GND)
		SoDeRa-PCIe_1v0.G3				L4  (Signal/PWR/GND)
		SoDeRa-PCIe_1v0.G4				L5  (Signal/PWR/GND)
		SoDeRa-PCIe_1v0.G5				L6  (PWR/GND)
		SoDeRa-PCIe_1v0.G6				L7  (PWR/GND)	
		SoDeRa-PCIe_1v0.G7				L8  (Signal/PWR/GND)
		SoDeRa-PCIe_1v0.G8				L9  (GND/PWR)
		SoDeRa-PCIe_1v0.G9				L10 (CLK/Signal)
		SoDeRa-PCIe_1v0.G10				L11 (GND)
		SoDeRa-PCIe_1v0.GBL				Bottom (Signal/PWR/GND)

		 
		SoDeRa-PCIe_1v0.GPB				Bottom Pad Master
		SoDeRa-PCIe_1v0.GPT				Top Pad Master

		SoDeRa-PCIe_1v0.GTO				Top Overlay
		SoDeRa-PCIe_1v0.GTP				Top Paste
		SoDeRa-PCIe_1v0.GTS				Top Solder

 
		SoDeRa-PCIe_1v0.GBS				Bottom Solder
		SoDeRa-PCIe_1v0.GBP				Bottom Paste
		SoDeRa-PCIe_1v0.GBO				Bottom Overlay


		SoDeRa-PCIe_1v0.GM1				Mechanical 1 (Board Cutout)


		SoDeRa-PCIe_1v0.GM14				ASM BOT (Assembly bottom)
		SoDeRa-PCIe_1v0.GM15				ASM TOP (Assembly top)
		
  
Important Notes
---------------
0.35mm ring and 0.2mm drill via-in-pads must be resin filled with metal cap (IC1).

IC1 thermal pad vias must NOT be resin filled with metal cap.

DRCs must be run on Gerber files before building boards.

All through hole vias may be plated shut.

Solder mask : dark blue, both sides, halogen free, glossy finish (NOT matte).

Silkscreen : white epoxy ink, halogen free, both sides. No silkscreen on pads.

Electrical test : 100 % netlist.

Boards are to be individually bagged.

Design software used:  Altium Designer 15.0 

Controlled Impedance
--------------------

  * 100 Ohm coupled microstrip line (Top layer) characteristics:
    Top layer copper foil thickness: 17.5 um
	Track width = 0.2 mm (6.8 mils)
	Track spacing = 0.14 mm (5.51 mils)
	Track width/spacing ratio = 1.428
	Dielectric thickness from top to L2 = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
	
	Approximate coupled microstrip line impedance = 100.752 Ohms (+/- 10% tolerance)
	
  * 50 Ohm microstrip line (Top layer) characteristics:
    Top layer copper foil thickness: 17.5 um
	Track width = 0.309 mm (12.16 mils)
	Track width/spacing ratio = 1.786
	Dielectric thickness from top to L2 = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
	
	Approximate microstrip line impedance = 49.9998 Ohms (+/- 10% tolerance)
	
  * 85 Ohm coupled microstrip line (Top layer, PCI traces) characteristics:
    Top layer copper foil thickness: 17.5 um
	Track width = 0.3 mm (11.81 mils)
	Track spacing = 0.2 mm (6.8 mils)
	Track width/spacing ratio = 1.5
	Dielectric thickness from Top to 2nd layer = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
	
	Approximate coupled microstrip line impedance = 85 Ohms (+/- 10% tolerance)	
	
  * 85 Ohm coupled microstrip line (Bottom layer, PCI traces) characteristics:
    Bottom layer copper foil thickness: 17.5 um
	Track width = 0.3 mm (11.81 mils)
	Track spacing = 0.2 mm (6.8 mils)
	Track width/spacing ratio = 1.5
	Dielectric thickness from L11 to Bottom layer = 173um (6.8 mils)
	Dielectric between L11 layer and Bottom layer relative permittivity (Er): 4.2
	
	Approximate coupled microstrip line impedance = 85 Ohms (+/- 10% tolerance)