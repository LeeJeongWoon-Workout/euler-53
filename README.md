# euler-53

dic={0:1,1:1,2:2,3:6}
t=0

def factorial(n):
    global t
    t+=1
    if n in dic:
        return dic[n]
    else:
        output=n*factorial(n-1)
        dic[n]=output
        return output

count=0
for i in range(1,101):
    for j in range(1,i+1):
        result=factorial(i)/(factorial(i-j)*factorial(j))
        if result>1000000:
            count+=1

print(count)
print(t)
