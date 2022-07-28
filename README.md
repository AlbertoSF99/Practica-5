# Práctica 5 - Creación de un función con Azure Functions

## Innovaccion Virtual (VII Edición) #IAWizards

### Semana 2 - Sesión 4

En esta práctica se realizó una función sencilla desde la nube de Azure con Azure Function

-----------------------------------------------------------

#### Requerimientos 

- Cuenta de Azure con suscripción.
- Alguna extensión o programa para probar REST API's y HTTP como [Talend API Tester](https://chrome.google.com/webstore/detail/talend-api-tester-free-ed/aejoelaoggembcahagimdiliamlcdmfm)

-----------------------------------------------------------

#### Pasos a seguir

1. Ingresar a portal.azure.com y busca ‘Aplicación de funciones’ o ‘Azure Functions’ y pulsamos en ‘Crear’. Llenamos los campos necesarios (Suscripción, grupo de recursos, nombre de la aplicación de funciones, pila del entorno en tiempo de ejecución: Node.js, región, SO, tipo de plan: Serverless). Le damos en ‘Revisar y crear’ y en ‘Crear’.

![P5I1](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2001.PNG)

2. Una vez se haya creado, entramos al recurso y en el apartado de funciones creamos una función, en la cual escogemos como plantilla a ‘HTTP trigger’.

![P5I2](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2002.PNG)

3. Seleccionamos ahora el apartado de ‘Código y prueba’ y nos aparecerá un programa en código Node.js, le damos en ‘Probar/ejecutar’ y en el apartado de cuerpo podremos cambiar el texto a mostrar (está redactado en color naranja) y después, le damos en ‘Ejecutar’. Con esto comprobamos la ejecución de nuestra función. También podremos modificar en la programación, el mensaje que se mostrará con el disparador previamente elaborado cuando esté guardado.

![P5I3](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2003.PNG)

![P5I4](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2004.PNG)

![P5I5](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2005.PNG)

![P5I6](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2006.PNG)

4. Ubicamos la opción de ‘Obtener la dirección URL de la función’, la copiamos y debemos de descargar en nuestro navegador la extensión ‘Talend API Tester’. Abrimos dicha extensión y en donde diga ‘SCHEME’ pegamos el URL copiado previamente. En ‘METHOD’ seleccionamos ‘POST’ y en el apartado ‘BODY’ escribimos al lado de donde dice ‘Name’ el trigger que habíamos creado antes. Si le damos en ‘Send’ veremos que deniega esta acción debido a que no contamos con los permisos para realizar esto.

![P5I7](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2007.PNG)

![P5I8](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2008.PNG)

![P5I9](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2009.PNG)

5. Regresamos al portal de Azure, donde estábamos, nos dirigimos a ‘Claves de función’ y copiamos el valor de la clave que aparece como ‘default’ y regresando a la extensión, desde la opción de ‘Add authorization’ le damos en ‘Add header’. Como nombre pondremos “x-functions-key” y de valor se pone la key copiada.

![P5I10](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2010.PNG)

![P5I11](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2011.PNG)

![P5I12](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2012.PNG)

![P5I13](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2013.PNG)

![P5I14](https://github.com/AlbertoSF99/Practica-5/blob/main/Images/Sesi%C3%B3n%204%20-%20P5%2014.PNG)

***Información Adicional:*** Azure Functions es serverless. Se ejecuta cada vez que se mande a llamar, por lo tanto, el cobro es por operación y no por tiempo.
