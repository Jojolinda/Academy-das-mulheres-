# Academy-das-mulheres-
import tkinter as tk
from tkinter import messagebox

# Função para exibir o dia escolhido
def escolher_dia(dia):
    messagebox.showinfo("Dia Escolhido", f"Você escolheu ir à academia na {dia}.")

# Configuração da janela principal
root = tk.Tk()
root.title("Escolha um dia para ir à academia")

# Título
label = tk.Label(root, text="Escolha um dia da semana para ir à academia:", font=("Helvetica", 14))
label.pack(pady=20)

# Lista de dias da semana
dias = ["Segunda-feira", "Terça-feira", "Quarta-feira", "Quinta-feira", "Sexta-feira", "Sábado", "Domingo"]

# Criação dos botões
for dia in dias:
    button = tk.Button(root, text=dia, command=lambda d=dia: escolher_dia(d), width=20, font=("Helvetica", 12))
    button.pack(pady=5)

# Execução da aplicação
root.mainloop()
