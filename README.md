import tkinter as tk
from tkinter import messagebox


# Function to handle user registration
def register():
    username = username_entry.get()
    password = password_entry.get()

    # Add code to store the username and password in a database or any other suitable storage mechanism

    messagebox.showinfo("Registration", "Registration successful!")


# Function to handle user login
def login():
      username = login_username_entry.get()
      password = login_password_entry.get()


    # Add code to validate the entered username and password against the stored credentials

    messagebox.showinfo("Login", "Login successful!")


# Function to handle task creation
def create_task():
    title = title_entry.get()
    description = description_entry.get("1.0", tk.END)
    due_date = due_date_entry.get()

    # Add code to store the task details in a database or any other suitable storage mechanism

    messagebox.showinfo("Task Creation", "Task created successfully!")


# Create the main window
window = tk.Tk()
window.title("Task Management System")

# User Management Section
user_frame = tk.Frame(window)
user_frame.pack(pady=10)

username_label = tk.Label(user_frame, text="Username:")
username_label.grid(row=0, column=0, padx=5, pady=5)
username_entry = tk.Entry(user_frame)
username_entry.grid(row=0, column=1, padx=5, pady=5)

password_label = tk.Label(user_frame, text="Password:")
password_label.grid(row=1, column=0, padx=5, pady=5)
password_entry = tk.Entry(user_frame, show="*")
password_entry.grid(row=1, column=1, padx=5, pady=5)

register_button = tk.Button(user_frame, text="Register", command=register)
register_button.grid(row=2, column=0, padx=5, pady=5)
login_button = tk.Button(user_frame, text="Login", command=login)
login_button.grid(row=2, column=1, padx=5, pady=5)

# Task Management Section
task_frame = tk.Frame(window)
task_frame.pack(pady=10)

title_label = tk.Label(task_frame, text="Title:")
title_label.grid(row=0, column=0, padx=5, pady=5)
title_entry = tk.Entry(task_frame)
title_entry.grid(row=0, column=1, padx=5, pady=5)

description_label = tk.Label(task_frame, text="Description:")
description_label.grid(row=1, column=0, padx=5, pady=5)
description_entry = tk.Text(task_frame, height=5, width=30)
description_entry.grid(row=1, column=1, padx=5, pady=5)

due_date_label = tk.Label(task_frame, text="Due Date:")
due_date_label.grid(row=2, column=0, padx=5, pady=5)
due_date_entry = tk.Entry(task_frame)
due_date_entry.grid(row=2, column=1, padx=5, pady=5)

create_task_button = tk.Button(task_frame, text="Create Task", command=create_task)
create_task_button.grid(row=3, column=0, columnspan=2, padx=5, pady=5)

# Start the GUI event loop
window.mainloop()

#image![Screenshot (2)](https://github.com/Yash-Vidyasagar/Build-a-Task-Management-
System-/assets/133989694/21857e6d-4c3c-4d2c-b119-17994f196e21)


#image![Screenshot (3)](https://github.com/Yash-Vidyasagar/Build-a-Task-Management-System-/assets/133989694/1ecb69eb-c91e-4bb7-9ca3-2a3159424c47)

