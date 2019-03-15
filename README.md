# calci
It's a simple calculator 
from tkinter import*
def btnclick(number):
    global operator
    operator=operator+str(number)
    txt_Input.set(operator)
def btnclrdisplay():
    global operator
    operator=""
    txt_Input.set("")
def btnequalinput():
    global operator
    sumup=str(eval(operator))
    txt_Input.set(sumup)
    operator=""
cal=Tk()
cal.title("Calculator")
operator=""
txt_Input=StringVar()
txtDisplay=Entry(cal,font=('arial',20,'bold'),textvariable=txt_Input,bd=10,insertwidth=1,
                bg="powder blue",justify="right",).grid(columnspan=4)
btn7=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="7",command=lambda:btnclick(7)).grid(row=1,column=0)
btn8=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="8",command=lambda:btnclick(8)).grid(row=1,column=1)
btn9=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="9",command=lambda:btnclick(9)).grid(row=1,column=2)

#########################################################################
btn4=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="4",command=lambda:btnclick(4)).grid(row=2,column=0)
btn5=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="5",command=lambda:btnclick(5)).grid(row=2,column=1)
btn6=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="6",command=lambda:btnclick(6)).grid(row=2,column=2)

##########################################################################
btn3=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="3",command=lambda:btnclick(3)).grid(row=3,column=0)
btn2=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="2",command=lambda:btnclick(2)).grid(row=3,column=1)
btn1=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="1",command=lambda:btnclick(1)).grid(row=3,column=2)
#######################################################################################3
btnclear=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
           text="C",command=btnclrdisplay).grid(row=4,column=0)


btndot=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text=".",command=lambda:btnclick(".")).grid(row=4,column=1)
btnequal=Button(cal,pady=16,padx=16,fg="black",font=("arial",20,"bold"),
            text="=",command=btnequalinput).grid(row=4,column=2)
#########################################################################
add=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="+",command=lambda:btnclick("+")).grid(row=1,column=3)
sub=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="-",command=lambda:btnclick("-")).grid(row=2,column=3)
mul=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="*",command=lambda:btnclick("*")).grid(row=3,column=3)
div=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="/",command=lambda:btnclick("/")).grid(row=4,column=3)
mod=Button(cal,padx=16,pady=16,fg="black",font=("arial",20,"bold"),
            text="%",command=lambda:btnclick("%")).grid(row=1,column=3)
###############################################################################
cal.mainloop()
