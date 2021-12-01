# items-bill
shopping bill
class items:
    def __init__(self,name,quantity,unitprice,saleprice,yousave):
        self.name = name
        self.quantity = quantity
        self.unitprice = unitprice
        self.saleprice = saleprice
        self.yousave = yousave
    def displayproductdetails(self):
        print('{}  {}  {}  {}'.format(self.name,self.quantity,self.unitprice,self.saleprice))

print('item  quantity  price')
for i in range(4):
    name=input()
    quantity=int(input())
    if name=='milk':
        saleprice=(quantity/2)*5.00
        tot=(quantity/2)+(quantity/2)
        yousave=(tot*3.97)-saleprice
        unitprice=(quantity%2)*3.97
    if name=='bread':
        saleprice=(quantity/3)*6.00
        yousave=(tot*2.17)-saleprice
        unitprice=(quantity%3)*2.17
    if name=='banana':
        unitprice=quantity*0.99
    if name=='apple':
        unitprice=quantity*0.89
    res=items(name,quantity,saleprice,unitprice,yousave)
    res.displayproductdetails()
    
    
