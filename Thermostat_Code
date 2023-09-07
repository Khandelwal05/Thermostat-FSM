import tkinter as tk

class Thermostat:

    def __init__(self, master):
        self.master = master
        self.state = "off"

        self.label = tk.Label(master, text="Thermostat is off", height = 3, width = 20)
        self.label.pack()
        
        self.canvas = tk.Canvas(master,width=100, height=100,bg='lightblue')
        self.canvas.pack()

        self.light = self.canvas.create_oval(10, 20, 100, 100, fill="grey")

        # Entry widget for temperature input
        self.temp_entry = tk.Entry(master,width=30, font=('arial',15))
        self.temp_entry.pack(padx=20,pady=20)
        
        self.set_temp_button = tk.Button(master, text="Set Temperature", command=self.set_temp, height = 3, width = 20, font=('arial',15), bg='Violet')
        self.set_temp_button.pack()
        self.off_button = tk.Button(master, text="Turn off", command=self.turn_off, height = 3, width = 10, font=('arial',15),bg="black",fg="white")
        self.off_button.pack()
        
    def set_temp(self):
        temperature = float(self.temp_entry.get())
        if self.state == "off":
            if temperature > 25:
                self.state = "cooling"
                self.label.configure(text="Thermostat is cooling", font=('arial',15),bg='lightblue')
                self.canvas.itemconfigure(self.light, fill="blue")
            elif temperature < 20:
                self.state = "heating"
                self.label.configure(text="Thermostat is heating", font=('arial',15),bg='lightblue')
                self.canvas.itemconfigure(self.light, fill="red")
        elif self.state == "heating":
            if temperature >= 20:
                self.state = "off"
                self.canvas.itemconfigure(self.light, fill="white")
                self.label.configure(text="Thermostat is off", font=('arial',15),bg='lightblue')
        elif self.state == "cooling":
            if temperature <= 25:
                self.state = "off"
                self.canvas.itemconfigure(self.light, fill="white")
                self.label.configure(text="Thermostat is off", font=('arial',15),bg='lightblue',width=50)
                
    def turn_off(self):
        self.state = "off"
        self.canvas.itemconfigure(self.light, fill="white")
        self.label.configure(text="Thermostat is off", font=('arial',15),width=50,bg='lightblue')

root = tk.Tk()
root.geometry("500x400")
root.configure(bg='lightblue')
thermostat = Thermostat(root)
root.mainloop()
