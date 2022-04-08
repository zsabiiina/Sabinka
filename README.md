# Sabinka
My name
import math

goods_m = 1 # mass in kg

def load_mass(goods_m, fuel_good_coef=0.8, accuracy = 0.001):

    '''
    return mass of the load to be sent on the rocket including fuel
    accuracy is in kg
    '''
    
    n = math.floor(math.log(accuracy/goods_m, fuel_good_coef))
    m = goods_m # total mass of the rocket load
    add_mass = goods_m # mass of fuel needed to deliver given mass
    for _ in range(n):
        add_mass *= fuel_good_coef
        m += add_mass
    
    return m, m - goods_m

def print_masses(m):
    masses = load_mass(m)
    print(f"Delivery of {m} kg requires {masses[1]:.3f} kg of fuel. Total mass of the load will be {masses[0]:.3f} kg.")
    
print_masses(1)
print_masses(527)
