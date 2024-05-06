# king

import tkinter as tk
from tkinter import messagebox

def predict_ranges():
    # Get the three multiplier strings from the input fields
    multiplier1 = entry1.get()
    multiplier2 = entry2.get()
    multiplier3 = entry3.get()

    # Call your model to predict the ranges for future multipliers
    # Replace the following lines with your actual prediction logic
    predicted_range1 = "1.2-2.0"
    predicted_range2 = "2.0-5.0"
    predicted_range3 = "5.0-10"

    # Display the predicted ranges
    result_text = f"Predicted Range for Multiplier 1: {predicted_range1}\n"
    result_text += f"Predicted Range for Multiplier 2: {predicted_range2}\n"
    result_text += f"Predicted Range for Multiplier 3: {predicted_range3}"
    messagebox.showinfo("Predicted Ranges", result_text)

# Create the main window
root = tk.Tk()
root.title("Multiplier Predictor")

# Create input fields for three multipliers
entry1 = tk.Entry(root)
entry2 = tk.Entry(root)
entry3 = tk.Entry(root)

entry1.pack(pady=10)
entry2.pack(pady=10)
entry3.pack(pady=10)

# Create a button to trigger prediction
predict_button = tk.Button(root, text="Predict Ranges", command=predict_ranges)
predict_button.pack()

# Run the UI loop
root.mainloop()
