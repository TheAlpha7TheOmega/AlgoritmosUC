# AlgoritmosUC
Tarea de Github
python.file
password = input()
verificador = []
indice = input()
verificador_indice =[]
nuevo_numero = input()
verificador_orden_de_busqueda = []
orden_de_busqueda = input()
verificador_nuevo_numero = []
numeros=['1','2','3','4','5','6','7','8','9','0']
orden = ['True','False']
u = input()
w = input()
m = input()
for n in password:
    if n in numeros:
        verificador.append(n)
string_password = ''
for l in verificador:
    string_password += l
password = int(string_password)
for m in nuevo_numero:
    if m in numeros:
        verificador_nuevo_numero.append(m)
string_nuevo_numero = ''
for M in verificador_nuevo_numero:
    string_nuevo_numero += M
nuevo_numero = int(string_nuevo_numero)
for x in indice:
    if x in numeros:
        verificador_indice.append(x)
string_indice = ''
for L in verificador_indice:
    string_indice += L
indice = int(string_indice)
if 'True' in orden_de_busqueda:
    orden_de_busqueda = True
elif "False" in orden_de_busqueda:
    orden_de_busqueda = False
def cantidad_de_digitos(password):
    digitos = 0
    while password > 0:
        digitos += 1
        password = password//10
    print(digitos)
    return(digitos)
cantidad_de_digitos(password)
def en_posicion(password,indice,orden_de_busqueda):
    indice_a_buscar = indice
    if orden_de_busqueda == True:
        verificador.reverse()
        for position, digito in enumerate(verificador):
            if position == indice_a_buscar:
                digito = int(digito)
                print(digito)
                return digito
    else:
        for posicion, digito in enumerate(verificador):
           if posicion == indice_a_buscar:
               digito = int(digito)
               print(digito)
               return digito
en_posicion(password,indice,orden_de_busqueda)
def reemplazar(password,indice,nuevo_numero,orden_de_busqueda):
    #los elementos dentro de verificador estan en formato string, pero para poder operar con ellos como quiero,
    # debo pasarlos a int.
    int_verificador = []
    str_int_verificador = []
    for X in verificador:
        X = int(X)
        int_verificador.append(X)
    reverso = list(reversed(int_verificador))
    if orden_de_busqueda == True:
        for x in range(len(int_verificador)):
                int_verificador[indice] = nuevo_numero
        for n in int_verificador:
            n = str(n)
            str_int_verificador.append(n)
            reverso_string_password = list(reversed(str_int_verificador))
        string_new_password = ''
        for l in reverso_string_password:
            string_new_password += l
            new_password = int(string_new_password)
        print(new_password)
        return(new_password)
    else:
         for x in range(len(int_verificador)):
                 int_verificador[indice] = nuevo_numero
         for n in int_verificador:
             n = str(n)
             str_int_verificador.append(n)
         string_new_password = ''
         for l in str_int_verificador:
            string_new_password += l
         new_password = int(string_new_password)
         print(new_password)
         return(new_password)
reemplazar(password,indice,nuevo_numero,orden_de_busqueda)
