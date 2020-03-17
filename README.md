class Solution:
    def makeFrames(self, l):
        
        l1 = [] 
        for x in l: 
            if x not in l1: 
                l1.append(x) 
        count=0
        sum=0
        #print(l1)
        for i in range(len(l1)):
            if(l.count(l1[i])%2==0):
                if(l.count(l1[i])%4==0):
                    count+=1
                sum=sum+l.count(l1[i])
            else:
                sum=sum+l.count(l1[i])-1
        return(sum//4)
