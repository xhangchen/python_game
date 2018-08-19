def capture(l):
    time=-1
    count=0
    while not count==len(l):
        count=0
        flag=[0]*len(l)
        f2=[0]*len(l)
        for i in range(len(l)):
            if l[i][i]==0and f2[i]==0:
                count+=1
                for j in range(len(l)):
                    if l[i][j]==1 and flag[j]==0 and not l[j][j]==0:
                        f2[j]=1
                        l[j][j]-=1
                        flag[j]=1
        time+=1
    return time
#eg:
print(capture([[0, 1, 0, 1, 0, 1],
         [1, 1, 1, 0, 0, 0],
         [0, 1, 2, 0, 0, 1],
         [1, 0, 0, 1, 1, 0],
         [0, 0, 0, 1, 3, 1],
         [1, 0, 1, 0, 1, 2]]))
