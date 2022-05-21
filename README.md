# Caleb
class Geoscience:
    def __init__(self, name, salary = 0):
        self.name= name
        self.salary = salary
    def allowances(self, percent):
        self.salary = self.salary + (self.salary * 0.35)
    def work(self):
        print((self.name) + ' determines composition of celestial body')
    def __repr__(self):
        return '<Geoscience: name = %s, salary = %d>' % (self.name, self.salary)

class Astrophysicist(Geoscience):
    def __init__(self,name):
        Geoscience.__init__(self,name, 13500)
    def work(self):
        print((self.name) + ' works on space physics')

class Geologist(Geoscience):
    def __init__(self,name):
        Geoscience.__init__(self,name, 12600)
    def work(self):
        print((self.name) + ' examines samples')

class Geophysicist(Geoscience):
    def __init__(self,name):
        Geoscience.__init__(self,name,13200)
    def work(self):
        print((self.name) + ' analyzes physical parameters of samples')

for well in Geoscience,Astrophysicist, Geologist, Geophysicist:
    obj = well(well.__name__)
    obj.work()

Ray = Astrophysicist('Caleb')
print(Ray)

class planet:
    def __init__(self, name):
        self.name = name
    def composition(self, Astrophysicist):
        element = input('enter planet composition = ')
        print((element) + (Astrophysicist))
        print((self.name) + ' is made up of ' + (element))

class distance:
    def __init__(self, km):
        self.km = km

class cost:
    def __init__(self, km):
        self.km = km()
        print((self.km) * 2000000)

Venus = planet('Kepler-211g')
Venus.composition('Elliot')
