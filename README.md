print("==================================================")
print("   SISTEMA DE GESTÃO - II COMPETIÇÃO DA START     ")
print("==================================================")

# Loop principal para manter o menu funcionando até o usuário sair
while True:
    print("\nEscolha uma opção do sistema:")
    print("1 - Verificar capacidade do ônibus (Excursão)")
    print("2 - Calcular pontuação de leitura (Rodrigo e Ana)")
    print("3 - Distribuir prêmios (Figurinhas e Jogos)")
    print("4 - Validar peso da bagagem/carrinho")
    print("5 - Ferramentas extras (Idade e Área do Triângulo)")
    print("0 - Sair do sistema")
    
    opcao = input("\nDigite o número da opção desejada: ")

    # OPÇÃO 1: Controle de passageiros (if / else)
    if opcao == "1":
        print("\n--- CONTROLE DO ÔNIBUS ---")
        alunos = int(input("Digite a quantidade de alunos: "))
        monitores = int(input("Digite a quantidade de monitores: "))
        total_pessoas = alunos + monitores
        
        if total_pessoas <= 50:
            print(f"Total de {total_pessoas} pessoas. Status: PODE IR! (Vagas restantes: {50 - total_pessoas})")
        else:
            excesso = total_pessoas - 50
            print(f"Total de {total_pessoas} pessoas. Status: NÃO PODE IR! (Excedeu em {excesso} pessoas)")

    # OPÇÃO 2: Cálculo de pontos (Operações básicas)
    elif opcao == "2":
        print("\n--- PLACAR DE LEITURA ---")
        # Pontos do Rodrigo
        ficcao_rodrigo = int(input("Quantos livros de ficção Rodrigo leu? ")) * 10
        n_ficcao_rodrigo = int(input("Quantos de não-ficção Rodrigo leu? ")) * 8
        infantil_rodrigo = int(input("Quantos infantis Rodrigo leu? ")) * 6
        pontos_rodrigo = ficcao_rodrigo + n_ficcao_rodrigo + infantil_rodrigo
        
        # Pontos da Ana
        ficcao_ana = int(input("Quantos livros de ficção Ana leu? ")) * 8
        infantil_ana = int(input("Quantos infantis Ana leu? ")) * 6
        pontos_ana = ficcao_ana + infantil_ana
        
        print(f"\nResultado Rodrigo: {pontos_rodrigo} pontos")
        print(f"Resultado Ana: {pontos_ana} pontos")
        print(f"Soma total da equipe: {pontos_rodrigo + pontos_ana} pontos")

    # OPÇÃO 3: Divisão inteira (//) e Resto (%)
    elif opcao == "3":
        print("\n--- DISTRIBUIÇÃO DE PRÊMIOS ---")
        tipo = input("Deseja dividir (F)igurinhas ou (J)ogos? ").upper()
        
        if tipo == "F":
            total_fig = int(input("Total de figurinhas: "))
            amigos = int(input("Número de amigos: "))
            # João conta como 2 pessoas na divisão
            fig_amigo = total_fig // (amigos + 2)
            fig_joao = 2 * fig_amigo
            print(f"Cada amigo recebe {fig_amigo} figurinhas.")
            print(f"João recebe {fig_joao} figurinhas.")
        elif tipo == "J":
            total_jogos = int(input("Total de jogos: "))
            amigos = int(input("Número de amigos: "))
            por_amigo = total_jogos // amigos
            resto = total_jogos % amigos
            print(f"Cada amigo recebe {por_amigo} jogos e sobram {resto} na caixa.")
        else:
            print("Opção inválida! Digite F ou J.")

    # OPÇÃO 4: Validação de limite (if / else)
    elif opcao == "4":
        print("\n--- BALANÇA DO CARRINHO (MÁX 20KG) ---")
        peso1 = float(input("Peso do item 1 (kg): "))
        peso2 = float(input("Peso do item 2 (kg): "))
        total_peso = peso1 + peso2
        
        if total_peso <= 20:
            print(f"Peso total: {total_peso}kg. Os itens cabem no carrinho!")
        else:
            print(f"Peso total: {total_peso}kg. Excede o limite em {total_peso - 20}kg.")

    # OPÇÃO 5: Cálculos matemáticos diversos
    elif opcao == "5":
        print("\n--- FERRAMENTAS EXTRAS ---")
        # Idade futura
        idade = int(input("Sua idade atual: "))
        anos = int(input("Quantos anos quer avançar no tempo? "))
        print(f"-> Você terá {idade + anos} anos.")
        
        # Área do triângulo
        print("\nCálculo de Área do Triângulo:")
        base = float(input("Base: "))
        altura = float(input("Altura: "))
        area = (base * altura) / 2
        print(f"-> A área do triângulo é {area}.")

    # OPÇÃO 0: Encerrar o programa
    elif opcao == "0":
        print("\nEncerrando o sistema da Start... Até a próxima competição!")
        break

    # Caso o usuário digite algo que não existe no menu
    else:
        print("\nOpção inválida! Tente novamente.")
Use o código com cuidado.


                        
