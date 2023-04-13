import matplotlib.pyplot as plt

def high(h0, v0):
    h = h0 + v0 * dt
    return h

def velocity(v0, a0):
    v = v0 + a0 * dt
    return v

def acceleration(v0, g):
    a = g * (1 + v0 / 20)
    return a



print("This model usable for low height \nIt's use differential equations for basketball default :)")
print('Input start heigh of falling(in meters):')
h0 = float(input())
dt = h0/10000
g = -9.82
v0 = vs = hs = asr = t = 0
a0 = g

list_time = []
list_high = []
list_velocity = []
list_acceleration = []
list_time.append(t)
list_high.append(h0)
list_velocity.append(v0)
list_acceleration.append(a0)
while (h0 > 0):
    hs = high(h0, v0)
    vs = velocity(v0, a0)
    asr = acceleration(v0, g)
    a0 = asr
    v0 = vs
    h0 = hs
    t += dt
    list_time.append(t)
    list_high.append(h0)
    list_velocity.append(v0)
    list_acceleration.append(a0)

vel = abs(v0)
acc = abs(a0)
print("End acceleration:", acc, "m/s^2")
print("End velocity:", vel, "m/s")
print('Time of fall:', t, "s")


sp = plt.subplot(221)
plt.plot(list_time, list_high)
plt.grid(True)
plt.title(r'$high(t)$')

sp = plt.subplot(222)
plt.plot(list_time, list_velocity)
plt.grid(True)
plt.title(r'$velocity(t)$')

sp = plt.subplot(223)
plt.plot(list_time, list_acceleration)
plt.grid(True)
plt.title(r'$acceleration(t)$')

plt.show()

print('Press any key to exit')
s = input()
