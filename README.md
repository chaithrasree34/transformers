# transformers
# Transformer Calculator Using Python

print("TRANSFORMER CALCULATOR")
print("----------------------")

print("1. Calculate Secondary Voltage")
print("2. Calculate Turns Ratio")
print("3. Calculate Secondary Current")
print("4. Calculate Efficiency")

choice = int(input("\nEnter your choice (1-4): "))

if choice == 1:
    V1 = float(input("Enter primary voltage (V): "))
    N1 = float(input("Enter primary turns: "))
    N2 = float(input("Enter secondary turns: "))

    V2 = V1 * (N2 / N1)

    print("\nSecondary Voltage =", round(V2, 2), "V")

elif choice == 2:
    N1 = float(input("Enter primary turns: "))
    N2 = float(input("Enter secondary turns: "))

    turns_ratio = N1 / N2

    print("\nTurns Ratio =", round(turns_ratio, 2))

elif choice == 3:
    V1 = float(input("Enter primary voltage (V): "))
    V2 = float(input("Enter secondary voltage (V): "))
    I1 = float(input("Enter primary current (A): "))

    I2 = (V1 * I1) / V2

    print("\nSecondary Current =", round(I2, 2), "A")

elif choice == 4:
    output_power = float(input("Enter output power (W): "))
    input_power = float(input("Enter input power (W): "))

    efficiency = (output_power / input_power) * 100

    print("\nTransformer Efficiency =", round(efficiency, 2), "%")

else:
    print("\nInvalid choice!")