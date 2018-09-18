tran={(0,0):(0,3),(0,1):(1,3),(0,2):(2,3),(0,3):(3,3),
      (1,0):(0,2),(1,1):(1,2),(1,2):(2,2),(1,3):(3,2),
      (2,0):(0,1),(2,1):(1,1),(2,2):(2,1),(2,3):(3,1),
      (3,0):(0,0),(3,1):(1,0),(3,2):(2,0),(3,3):(3,0)}

def recall_password(t1,t2):
    s=''
    gri=[]
    r=[[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0]]
    for i in range(4):
        for j in range(4):
            if t1[i][j]=='X':
                r[i][j]=1
                s+=t2[i][j]

    for i in range(4):
        for j in range(4):
            if r[i][j]==1:
                gri.append((i,j))
    for k in range(3):
        gri2=[]
        for i in gri:
            gri2.append(tran[i])
        gri=gri2
        for i in range(4):
            for j in range(4):
                if (i,j) in gri:
                    s+=t2[i][j]
    return s

# eg:
print(recall_password(
    ('....' ,
     'X..X' ,
     '.X..' ,
     '...X' ),
    ('xhwc' ,
     'rsqx' ,
     'xqzz' ,
     'fyzr' )))






