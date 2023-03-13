from tkinter import*

def mainWindow():
    main=Tk()
    main.title("BMI App by Phoomtep Pitakamnuay")
    main.geometry('350x600')
    main.configure(bg='#35b0ab')
    main.option_add('*font', 'Helvetica 15 bold')
    main.columnconfigure(0, weight=1)
    main.rowconfigure((1,2,3), weight=4)
    main.rowconfigure(4, weight=1)
    return main

def frame():
    frm_height=Frame(main, bg='#1fab89')
    frm_height.grid(row=1, sticky='NEWS')
    frm_height.rowconfigure((0,1), weight=1)
    frm_height.columnconfigure(0, weight=1)
    frm_weight=Frame(main, bg='#62d2a2')
    frm_weight.grid(row=2, sticky='NEWS')
    frm_weight.rowconfigure((0,1), weight=1)
    frm_weight.columnconfigure(0, weight=1)
    frm_calculate=Frame(main, bg='#faffb8')
    frm_calculate.grid(row=3, sticky='NEWS')
    frm_calculate.rowconfigure(0, weight=1)
    frm_calculate.columnconfigure((0,1), weight=1)
    return frm_height, frm_weight, frm_calculate

def widget():
    Label(main, text="BMI App", bg='#35b0ab', fg='white').grid(row=0, sticky='NW', padx=10, pady=10)
    Label(frm_height, text="HEIGHT: (cm.)", font='Helvetica 20 bold', bg='#1fab89', fg='white').grid(row=0, sticky=W, padx=30)
    Label(frm_weight, text="WEIGHT: (kg.)", font='Helvetica 20 bold', bg='#62d2a2', fg='white').grid(row=0, sticky=W, padx=30)
    Entry(frm_height, width=20, justify=RIGHT, textvariable=height).grid(row=1, sticky='NW', padx=30)
    Entry(frm_weight, width=20, justify=RIGHT, textvariable=weight).grid(row=1, sticky='NW', padx=30)
    Label(frm_calculate, text='BMI =', font='Helvetica 20 bold', bg='#faffb8').grid(row=0, column=0, sticky=E)
    Label(frm_calculate, font='Helvetica 20 bold', bg='#faffb8', textvariable=bmi).grid(row=0, column=1, sticky=W)
    Button(main, text="Calculate", font='Helvetica 12 bold', bd=0, command=calculate).grid(row=4, sticky='NEWS', padx=10, pady=10)

def calculate():
    int_height=int(height.get())
    int_weight=int(weight.get())
    int_bmi=int_weight/(int_height/100)**2
    bmi.set("%.2f"%int_bmi)

main=mainWindow()
height=StringVar()
weight=StringVar()
bmi=StringVar()
bmi.set("")
frm_height, frm_weight, frm_calculate = frame()
widget()
main.mainloop()
