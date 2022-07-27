# Práctica 5 - Creación de un función con Azure Functions

## Innovaccion Virtual (VII Edición) #IAWizards

### Semana 2 - Sesión 4

-----------------------------------------------------------

#### Requerimientos 

- Cuenta de Azure con suscripción.
- Alguna extensión o programa para probar REST API's y HTTP como [Talend API Tester](https://chrome.google.com/webstore/detail/talend-api-tester-free-ed/aejoelaoggembcahagimdiliamlcdmfm)

-----------------------------------------------------------

#### Pasos a seguir

1. Ingresar a portal.azure.com y busca ‘Aplicación de funciones’ o ‘Azure Functions’ y pulsamos en ‘Crear’. Llenamos los campos necesarios (Suscripción, grupo de recursos, nombre de la aplicación de funciones, pila del entorno en tiempo de ejecución: Node.js, región, SO, tipo de plan: Serverless). Le damos en ‘Revisar y crear’ y en ‘Crear’.

![P5I1](Images\Sesión 4 - P5 01.PNG)

2. Una vez se haya creado, entramos al recurso y en el apartado de funciones creamos una función, en la cual escogemos como plantilla a ‘HTTP trigger’.

![P5I2](Images\Sesión 4 - P5 02.PNG)

3. Seleccionamos ahora el apartado de ‘Código y prueba’ y nos aparecerá un programa en código Node.js, le damos en ‘Probar/ejecutar’ y en el apartado de cuerpo podremos cambiar el texto a mostrar (está redactado en color naranja) y después, le damos en ‘Ejecutar’. Con esto comprobamos la ejecución de nuestra función. También podremos modificar en la programación, el mensaje que se mostrará con el disparador previamente elaborado cuando esté guardado.

![P5I3](Images\Sesión 4 - P5 03.PNG)

![P5I4](Images\Sesión 4 - P5 04.PNG)

![P5I5](Images\Sesión 4 - P5 05.PNG)

![P5I6](Images\Sesión 4 - P5 06.PNG)

4. Ubicamos la opción de ‘Obtener la dirección URL de la función’, la copiamos y debemos de descargar en nuestro navegador la extensión ‘Talend API Tester’. Abrimos dicha extensión y en donde diga ‘SCHEME’ pegamos el URL copiado previamente. En ‘METHOD’ seleccionamos ‘POST’ y en el apartado ‘BODY’ escribimos al lado de donde dice ‘Name’ el trigger que habíamos creado antes. Si le damos en ‘Send’ veremos que deniega esta acción debido a que no contamos con los permisos para realizar esto.

![P5I7](Images\Sesión 4 - P5 07.PNG)

![P5I8](Images\Sesión 4 - P5 08.PNG)

![P5I9](Images\Sesión 4 - P5 09.PNG)

5. Regresamos al portal de Azure, donde estábamos, nos dirigimos a ‘Claves de función’ y copiamos el valor de la clave que aparece como ‘default’ y regresando a la extensión, desde la opción de ‘Add authorization’ le damos en ‘Add header’. Como nombre pondremos “x-functions-key” y de valor se pone la key copiada.

![P5I10](Images\Sesión 4 - P5 10.PNG)

![P5I11](Images\Sesión 4 - P5 11.PNG)

![P5I12](Images\Sesión 4 - P5 12.PNG)

![P5I13](Images\Sesión 4 - P5 13.PNG)

![P5I14](Images\Sesión 4 - P5 14.PNG)

***Información Adicional:*** Azure Functions es serverless. Se ejecuta cada vez que se mande a llamar, por lo tanto, el cobro es por operación y no por tiempo.