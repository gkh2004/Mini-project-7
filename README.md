# Mini-project-7
MARKS ADDING

import csv

file = open('marks.csv','r')

csvreader= csv.reader(file)

header = next(csvreader)

totalmarks={}

for row in csvreader:

  x=row[0]
  
  if x in totalmarks:
  totalmarks[x]=totalmarks[x] + int(row[1])
  else:
      totalmarks[x]= int(row[1])

print(totalmarks)
