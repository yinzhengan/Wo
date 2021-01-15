# Wo

KERN_DIR = /lib/modules/$(shell uname -r)/build
 
all:
	make -C $(KERN_DIR) M=`pwd` modules
 
clean:
	make -C $(KERN_DIR) M=$(shell pwd) modules clean
	rm -rf modules.order
 
obj-m := virtualport.o






from tkinter import *

def center_window(w = 500, h = 300):
    ws = root.winfo_screenwidth()
    hs = root.winfo_screenheight()
    x = (ws/2) - (w/2)
    y = (hs/2) - (h/2)
    root.geometry("%dx%d+%d+%d" % (w, h, x, y))

root = Tk(className='郑建国 201752030120')
label = Label(root)
label['text'] = 'Intel(R) Core(TM) i5-7300HQ CPU @ 2.50GHz\n5.4.0-42-generic'
label.pack()

center_window(500, 300)
root.mainloop()
