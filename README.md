# Discount-function-for-prime-non-prime-members
This code calculates the discount for prime/ non-prime members on online shopping site

def blk_fri(int_value):
 q=int_value-0.08*int_value #Made a simple formula for calculating discount price (for non prime memebers)
 return q

def prime(int_value):
 p=int_value-0.23*int_value//1 #Made a simple formula for calculating discount price (for prime memebers = 23% + additional seasonal discount)
 return p


#int_value=float(input("Enter the price of the product you wanna buy: "))
while True:
 try:
  int_value=float(input("Enter the price of the product you wanna buy: ")) #Becasue websites have prices feeded already, it doesn't need to have this condition. But I've included it for this test code.
  break #If the input is in nubers, the loop will break, and the value will go for further processing
 except:
  print("\nPlease give input in numbers")


ifprime=prime(int_value) #Defined variables for using various discounts
blkdefault=blk_fri(int_value)

print("\nHurray! It's Black Friday Sale! Your total amount after getting 8% discount is",(round(blkdefault,2)),"\nBut wait! there's more! If you buy our prime membership, you'll get 23% discount as default,\n+ special seasonal discounts like today's (additional 8%) which means you'll only have to pay", (round(ifprime,2)),"\n\nJOIN THE PRIME FAMILY NOW!")
