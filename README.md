# Sabinka
My name
import math

goods_b = 1 # mass in kg

def load_mass(goods_b, fuel_good_coef=0.8, accuracy = 0.001):

    '''
    return mass of the load to be sent on the rocket including fuel
    accuracy is in kg
    '''
    
    a = math.floor(math.log(accuracy/goods_b, fuel_good_coef))
    b = goods_b # total mass of the rocket load
    add_mass = goods_b # mass of fuel needed to deliver given mass
    for _ in range(n):
        add_mass *= fuel_good_coef
        b += add_mass
    
    return b, b - goods_b

def print_masses(b):
    masses = load_mass(b)
    print(f"Delivery of {b} kg requires {masses[1]:.3f} kg of fuel. Total mass of the load will be {masses[0]:.3f} kg.")
    
print_masses(1)
print_masses(527)
