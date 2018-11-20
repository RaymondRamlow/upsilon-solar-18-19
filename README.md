# upsilon-solar-18-19
import time
class Solarcell(object):
  def __init__(self, material, bandgap, inducedV, valence, cost,particles):
    self.material = material #string that is the name of the material
    self.bandgap = bandgap #in electron volts (eV)
    self.valence = valence #valence electron energy (we can use this for the physics of the photons hitting the electrons)
    self.cost = cost
    self.inducedV = inducedV
    self.particles = particles

class Particle(object):
    def __init__(self, material, bandgap, valence, posx, posy):
        self.material = material #string that is the name of the material
        self.bandgap = bandgap
        self.valence = valence #valence electron energy (we can use this for the physics of the photons hitting the 
        self.posx = posx #posx and posy describe the top left corner of the particle
        self.posy = posy

    def setpos(self, x, y):
        self.posx = x
        self.posy = y

    def getvel(self):
        return self.vel

class Conditions:
  def __init__(self, temp, sunnydays, humidity, intensity):
    self.temp = temp
    self.sunnydays = sunnydays
    self.hum = humidity
    self.elev = elevation
    self.inten = intensity

material = "silicon"
bandgap = 1.1
inducedV = 1
valence = 1
cost = 100
vel = 0

# we'll make the individual particles as 1 x 1 blocks for now, to keep things simple-ish
# to visualize what I've done:  I have a row of atoms represented by 1 x 1 cubes
# with top left corners at (posx,posy). They are stationary. As y'all fiddle with the code
# and expand upon it, think about assumptions we can make to make our lives easy (ex:  perfectly
# elastic collisions), which should help simplify creating photons and having them hit the material atoms


particles = []
silicon = Solarcell(material, bandgap, inducedV, valence, cost, particles)
for i in range(1,11):
    posx = i
    posy = 1
    newpart = Particle(material, bandgap, valence, posx, posy, vel)
    particles.append(newpart)

for part in siliconparts:
    print(part.posx , part.posy)
