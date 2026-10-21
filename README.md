# GEAR-DESIGN-CALCULATOR
Gear Design Calculator for designing suitable gear for the machines

# Mechanical Engineering: Gearbox Design Calculator

def calculate_gearbox(module, pinion_teeth, gear_teeth):
    pinion_diameter = module * pinion_teeth
    gear_diameter = module * gear_teeth

    center_distance = (pinion_diameter + gear_diameter) / 2
    gear_ratio = gear_teeth / pinion_teeth

    print("\n--- GEARBOX DESIGN RESULTS ---")
    print(f"Pinion pitch diameter: {pinion_diameter} mm")
    print(f"Gear pitch diameter: {gear_diameter} mm")
    print(f"Centre distance: {center_distance} mm")
    print(f"Gear reduction ratio: {gear_ratio}:1")


module = float(input("Enter gear module (mm): "))
pinion_teeth = int(input("Enter pinion teeth: "))
gear_teeth = int(input("Enter driven gear teeth: "))

if module > 0 and pinion_teeth > 0 and gear_teeth > 0:
    calculate_gearbox(module, pinion_teeth, gear_teeth)
else:
    print("Enter positive values only.")

