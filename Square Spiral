def getc(x):          #获得数x相对1的坐标
    if x==1:
        return [0,0]
    l=[]
    for i in range(33,0,-2):
        if x>(i-2)**2:
            if x<=i*i-3*i+3:
                b=(i-1)/2
                a=x-i*i+(i-1)*7/2
                break
            elif i*i-3*i+3<x<=i*i-2*(i-1):
                a=(i-1)/2
                b=i*i-(i-1)*5/2-x
                break
            elif i*i-2*i+2<x<=i*i-(i-1):
                b=(1-i)/2
                a=i*i-(i-1)*3/2-x
                break
            else:
                a=(1-i)/2
                b=x-i*i+(i-1)/2
                break
    l+=[a,b]
    return l

def find_distance(f,s):
    a=getc(f)
    b=getc(s)
    return abs(a[0]-b[0])+abs(a[1]-b[1])
#eg:
print(find_distance(5,9))
