Repositorio com versões executáveis client de PIR


v0.0.1 -> 05/05/2025 = Primeira versão app  
v0.0.2 -> 05/05/2025 = Resolução bug conexão com servidor de mesma rede e mudanças de diálogo  
v0.0.3 -> 07/05/2025 = Implementação função pot na batalha e mudanças de diálogo  
v0.0.4 -> ../05/2025 = Versão para apresentação em sala, ip servidor da utfpr

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
