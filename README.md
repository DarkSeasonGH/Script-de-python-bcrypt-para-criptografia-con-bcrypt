# Script-de-python-bcrypt-para-criptografia-con-bcrypt
Os dejo adjuntado al repositorio un script muy simple para que veais como funciona el tema de los hash.



Aqui teneis el codigo por si no podeis usar el archivo.py:



#Este script es para generar un hash de un mensaje que nos de el usuario
#Lo vamos a hacer usando la biblioteca de bcrypt

#Importamos la biblioteca
import bcrypt

#Le pedimos el mensaje al usuario
texto_usuario = input("Introduce un texto para que pueda ser hasheado por favor -->")

#Pasamos a bytes
password = texto_usuario.encode('utf-8')

#Generamos el hasheo con bcrypt 
hasheo = bcrypt.hashpw(password,bcrypt.gensalt())

#Imprimimos el resultado
print("El resultado del hasheo es: " +str(hasheo))
