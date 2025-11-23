# Interface-em-PYTHON
# LoginApp  Este é um projeto de estudo em Python utilizando **PySimpleGUI**.    ## Sobre o projeto - Cria uma interface gráfica simples para capturar dados do usuário (Nome e Idade).   - Aplica conceitos de classes, métodos, eventos e organização de layout.   - Projeto inicial enquanto aprendo Python e busco explorar diferentes áreas na prática.


import PySimpleGUI as sg

class TelaPython:
    def __init__(self):
        # layout
        layout = [
            [sg.Text('Nome'), sg.Input(key='nome')],
            [sg.Text('Idade'), sg.Input(key='idade')],
            [sg.Button('Enviar')]
        ]
        
        # janela
        self.janela = sg.Window("Dados do Usuário", layout)

    def Iniciar(self):
        evento, valores = self.janela.read()
        if evento == sg.WINDOW_CLOSED:
            return
        print(valores)

if __name__ == "__main__":
    tela = TelaPython()
    tela.Iniciar()
