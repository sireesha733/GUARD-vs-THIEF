# GUARD-vs-THIEF
import math

def distance_from_origin(x, y):
    return math.sqrt(x**2 + y**2)

def main():
    num_thieves = int(input("Enter the number of thieves: "))
    caught_thieves = []

    for i in range(num_thieves):
        x, y = map(int, input(f"Enter the coordinates of thief {i+1} (x y): ").split())
        distance = distance_from_origin(x, y)
        catch_distance = int(input("Enter the catch distance: "))
        if distance <= catch_distance:
            caught_thieves.append((x, y))

    if caught_thieves:
        print("Thieves caught at the following positions:")
        for thief in caught_thieves:
            print(thief)
    else:
        print("No thieves were caught.")

if __name__ == "__main__":
    main()
