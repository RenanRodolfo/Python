# Python

http://pythonclub.com.br/gerenciando-banco-dados-sqlite3-python-parte1.html


# Utilização de menus
global What_comprar
What_comprar = []
global What_vender
What_vender = []


def submenu_um():
  # Put your submenus her
  
        while True:
          submenu_um=input("Você está no submenu 1 ?\n (1)Comprar\n (2)Vender\n (3)Voltar Menu Principal\n ")
          if submenu_um == "1":
            submenu_um_um()            
          elif submenu_um == "2":
            submenu_um_dois()
          elif submenu_um == "3":
            submenu_main()
  #pass

def submenu_dois():
  # Put your submenus her
  
        while True:
          submenu_dois=input("Você está no submenu 2 \n (1)Alugar\n (2)Emprestar\n (3)Voltar Menu Principal\n ")
          if submenu_dois == "1":
            submenu_buy()            
          elif submenu_dois == "2":
            submenu_sell()
          elif submenu_dois == "3":
            submenu_main()
  #pass        

def submenu_main():
  # Put your submenus her
  
        while True:
          main=input("\n Você está no menu principal\n (1)Comprar ou Vender\n (2)Alugar ou emprestar\n (3)Verificar Dados\n (4)Sair\n ")
          if main == "1":
            submenu_um()            
          elif main == "2":
            submenu_dois()
          elif main == "3":
             print("\n")
             try:                     
                     print("Você comprou: " ,What_comprar)
             except NameError:
                     print("Não comprou nada ")
                     
             try:                     
                     print("Você vendeu: " ,What_vender)
             except NameError:
                     print("Não vendeu nada\n\n")       
                     
          elif main == "4":
            break  
  #pass


def submenu_um_um():
  # Put your submenus her     

     while 1:
         What_comprar.append(input("O que você deseja comprar?\n"))
         contador = input("Digite 1 para cancelar as compras ou 2 para continuar comprando")
         if(contador == "1"):
                submenu_main()
                break
         elif(contador == "2"):
                submenu_um_um()
                
  #pass
        
def submenu_um_dois():
  # Put your submenus her  
     
                What_vender.append(input("O que você deseja vender?\n")) 
                submenu_main()
  #pass



while True:
  playermenumain=input("What would you like to do?\n (1)Comprar ou Vender\n (2)Alugar ou emprestar\n (3)Sair\n")
  if playermenumain == "1":
    submenu_um()    
  elif playermenumain == "2":
    submenu_dois()   
  elif playermenumain == "3":
    break

