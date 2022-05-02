# Insurance-CSV

import csv

with open('insurnace.csv', 'r') as csv_file:
    csv_reader = csv.reader(csv_file)
    
    with open('new_insurance.csv', 'w') as new_file:
        fieldnames = ['USER_ID', 'first_name', 'last_name', 'insurance']
        csv.writer.writerow()
    

lines = list()

members= input("Please enter a member's name to be deleted.")

with open('insurance_csv.csv', 'r') as readFile:

    reader = csv.reader(readFile)

    for row in reader:

        lines.append(row)

        for field in row:

            if field == members:

                lines.remove(row)

with open('Insurance_csv.csv', 'w') as writeFile:

    writer = csv.writer(writeFile)

    writer.writerows(lines)
