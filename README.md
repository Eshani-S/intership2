import datetime

current_date_and_time = datetime.datetime.now()
cdt = str(current_date_and_time)
k = cdt.replace(":", "-")
extension = ".txt"

file_name = k[:19] + extension
file = open(file_name, 'w')

n = int(input("Number of people: "))

while n>0:
    name = input("Name: ")
    number = str(input("Phone number: "))
    place = input("Place: ")
    temperature = str(float(input("Temperature in celsius: ")))
    print("\n")

    file.write("Name         : " + name + "\n")
    file.write("Phone number : " + number + "\n")
    file.write("Place        : " + place + "\n")
    file.write("Temperature  : " + temperature + "\n\n")
    n -= 1

file.close()
