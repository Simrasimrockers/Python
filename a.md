```c
file = open("Raja.csv","w")
print("Student Data")
name = input("Enter Student Name : ")
id = input("Enter Student id : ")
pno = input("Enter Student pno : ")
file.write(name)
file.write(id)
file.write(pno)
file.close()
```
