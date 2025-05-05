Repositorio com versões executáveis client de PIR


v0.0.1 -> 05/05/2025

import threading

parar_servidor = False

def monitorar_encerramento():
    global parar_servidor
    while True:
        comando = input("Digite 'sair' para encerrar o servidor")
        if comando.lower() == 'sair':
            parar_servidor = True
            break


threading.Thread(target=monitorar_encerramento, daemon=True).start()
