# Fraction-number
#By using Python magic method, arithmetic operation of two
#fraction numbers.

class Fraction:
    def __init__(self,n,d):
        self.num = n
        self.den = d
    
    def __str__(self):
        return "{}/{}".format(self.num,self.den)
    def __add__(self,other):
        temp_num = self.num * other.den + other.num*self.den
        temp_den = self.den * other.den
        return "{}/{}".format(temp_num,temp_den)
    def __sub__(self,other):
        temp_num = self.num*other.den - self.den*other.num
        temp_den = self.den * other.den
        return "{}/{}".format(temp_num,temp_den)
    
if __name__ == "__main__":
    fraction1 = Fraction(5,7)
    fraction2 = Fraction(6,8)
    print(fraction1)
    print(fraction2)
    print(fraction1 + fraction2)
    print(fraction1 - fraction2)
