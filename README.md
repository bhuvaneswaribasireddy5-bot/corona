# corona
# Python Program for Corona Inception Voltage

import math

print("CORONA INCEPTION VOLTAGE CALCULATOR")
print("------------------------------------")

# Input values
m0 = float(input("Enter surface irregularity factor (m0): "))
delta = float(input("Enter air density factor (δ): "))
r = float(input("Enter conductor radius (cm): "))
D = float(input("Enter conductor spacing (cm): "))

# Breakdown strength of air
g0 = 21.1   # kV/cm

# Calculate disruptive critical voltage
Vd = m0 * delta * g0 * r * math.log(D / r)

# Calculate line-to-line voltage
VLL = math.sqrt(3) * Vd

# Display results
print("\n--- RESULTS ---")
print("Disruptive Critical Voltage =", round(Vd, 2), "kV")
print("Corona Inception Line Voltage =", round(VLL, 2), "kV")
