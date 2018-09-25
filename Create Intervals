def create_intervals(li):
    ans=[]
    if len(li)==0:
        return ans
    l=list(sorted(li))
    if len(l)==1:
        return ans+[(l[0],l[0])]
    left=l[0]
    right=l[0]
    for i in range(len(l)-1):
        if l[i+1]-l[i]>1:
            ans+=[(left,right)]
            left=l[i+1]
            right=left
        else:
            right=l[i+1]
    if not left==right:
        ans+=[(left,right)]
    if l[-1]-l[-2]>1:
        ans+=[(l[-1],l[-1])]
    return  ans
#eg:
print(create_intervals([3]))
