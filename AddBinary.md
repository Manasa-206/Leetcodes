class Solution(object):
    def addBinary(self, a, b):
        a_int = int(a, 2)  
        b_int = int(b, 2)  
        sum_int = a_int + b_int  
        return bin(sum_int)[2:]  
            
