class Grade:
    grade1 = 0
    grade2 = 0
    grade3 = 0
    grade4 = 0 

from grade import Grade

class Student:

    def GetAvg(sum, n):
        return sum / n

    students = []
    n = int(input('Enter number of student: '))
    i = 0

    while i < int(n):

        gr = Grade

        name = input("Enter Name: ")
        gr.grade1 = float(input('Enter Grade 1: '))
        gr.grade2 = float(input('Enter Grade 2: '))
        gr.grade3 = float(input('Enter Grade 3: '))
        gr.grade4 = float(input('Enter Grade 4: '))
        sum = gr.grade1 + gr.grade2 + gr.grade3 + gr.grade4

        record = f'\nName: {name} \nGrade1: {gr.grade1} \nGrade2: {gr.grade2} \nGrade3: {gr.grade3} \nGrade4: {gr.grade4} \nAverage: {GetAvg(sum, 4)}\n'
        students.append(record)
        i += 1
        
    print()
    print()

    for s in students:
        print(s)

    view = int(input('Enter record number to view: '))
    print(students[view - 1])
    print()

    delt = int(input('Enter record to delete: '))
    students.pop(delt - 1)

    print()
    for s in students:
        print(s)
