# Prime
#Efficient python code to find number of primes in a given range
k=int(input('Enter the value of k upto which you want to count no of primes:')
import math
import time
def is_prime(n):
if n<=1:
  return False
if n==2:
  return True
if n>2 and n%2==0:
  return False
 max_div=math.floor(math.sqrt(n))
 for i in range(3,1+max_div,2):
   if n%i==0:
      return False
  return True
  # Driver function
  t0=time.time()
  c=0 # counter 
  for n in range(1,k):
   x= is_prime(n)
   c=c+x
   print('Total number of primes in given range are:',c)
   t1=time.time()
   print('Time required': , t1-t0)
