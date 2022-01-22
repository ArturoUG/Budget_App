# Budget_App
Certificación

Español

Solicitud de presupuesto

La clase de categoría en budget.py puede crear instancias de objetos en función de diferentes categorías de presupuesto, como comida, ropa y entretenimiento. Cuando se crean objetos, se pasan en el nombre de la categoría. La clase tiene una variable de instancia llamada libro mayor que es una lista. La clase también contiene los siguientes métodos:

Un método de depósito que acepta una cantidad y una descripción. Si no se da una descripción, por defecto es una cadena vacía. El método agrega un objeto a la lista del libro mayor en forma de {"cantidad": cantidad, "descripción": descripción}.
Un método de retiro que es similar al método de depósito, pero la cantidad transferida se almacena en el libro mayor como un número negativo. Si no hay suficientes fondos, no se agrega nada al libro mayor. Este método devuelve True si se realizó el retiro y False en caso contrario.
Un método get_balance que devuelve el saldo actual de la categoría de presupuesto en función de los depósitos y retiros que se han producido.
Un método de transferencia que acepta una cantidad y otra categoría de presupuesto como argumentos. El método agrega un retiro con el monto y la descripción "Transferir a [Categoría de presupuesto de destino]". Luego, el método agrega un depósito a la otra categoría de presupuesto con el monto y la descripción "Transferir de [Categoría de presupuesto de origen]". Si no hay suficientes fondos, no se agrega nada a ninguno de los libros mayores. Este método devuelve True si se realizó la transferencia y False en caso contrario.
Un método check_funds que acepta una cantidad como argumento. Devuelve False si el monto es menor que el saldo de la categoría de presupuesto y devuelve True en caso contrario. Este método es utilizado tanto por el método de retiro como por el método de transferencia.
Cuando se imprime el objeto de presupuesto, muestra:

Una línea de título de 30 caracteres donde el nombre de la categoría está centrado en una línea de * caracteres.
Una lista de los artículos en el libro mayor. Cada línea muestra la descripción y la cantidad. Se muestran los primeros 23 caracteres de la descripción, luego la cantidad. La cantidad está alineada a la derecha, contiene dos lugares decimales y muestra un máximo de 7 caracteres.
Una línea que muestra el total de la categoría.
Aquí hay un ejemplo de la salida:

*************Food*************
initial deposit        1000.00
groceries               -10.15
restaurant and more foo -15.89
Transfer to Clothing    -50.00
Total: 923.96

Además de la clase Categoría, una función (fuera de la clase) llamada create_spend_chart toma una lista de categorías como argumento. Devuelve una cadena que es un gráfico de barras.

El gráfico muestra el porcentaje gastado en cada categoría pasada a la función. El porcentaje gastado se calcula solo con retiros y no con depósitos. En el lado izquierdo del gráfico hay etiquetas 0 - 100. Las "barras" en el gráfico de barras están formadas por el carácter "o". La altura de cada barra se redondea hacia abajo al 10 más cercano. La línea horizontal debajo de las barras va dos espacios más allá de la barra final. Cada nombre de categoría está verticalmente debajo de la barra. Hay un título en la parte superior que dice "Porcentaje gastado por categoría".

Esta función se puede probar con hasta cuatro categorías.

Mire el resultado de ejemplo a continuación.

Porcentaje gastado por categoría

100|          
 90|          
 80|          
 70|          
 60| o        
 50| o        
 40| o        
 30| o        
 20| o  o     
 10| o  o  o  
  0| o  o  o  
    ----------
     F  C  A  
     o  l  u  
     o  o  t  
     d  t  o  
        h     
        i     
        n     
        g     

Las pruebas unitarias para este proyecto están en test_module.py.

Desarrollo

Escriba su código en budget.py. Para el desarrollo, puede usar main.py para probar su clase de Categoría. Haga clic en el botón "ejecutar" y main.py se ejecutará.

Pruebas

Importamos las pruebas de test_module.py a main.py para su comodidad. Las pruebas se ejecutarán automáticamente cada vez que presione el botón "ejecutar".


Ingles

Budget Application

Category class in budget.py is able to instantiate objects based on different budget categories like food, clothing, and entertainment. When objects are created, they are passed in the name of the category. The class have an instance variable called ledger that is a list. The class also contains the following methods:

A deposit method that accepts an amount and description. If no description is given, it default to an empty string. The method appends an object to the ledger list in the form of {"amount": amount, "description": description}.
A withdraw method that is similar to the deposit method, but the amount passed in is stored in the ledger as a negative number. If there are not enough funds, nothing is added to the ledger. This method returns True if the withdrawal took place, and False otherwise.
A get_balance method that returns the current balance of the budget category based on the deposits and withdrawals that have occurred.
A transfer method that accepts an amount and another budget category as arguments. The method adds a withdrawal with the amount and the description "Transfer to [Destination Budget Category]". The method then adds a deposit to the other budget category with the amount and the description "Transfer from [Source Budget Category]". If there are not enough funds, nothing is added to either ledgers. This method returns True if the transfer took place, and False otherwise.
A check_funds method that accepts an amount as an argument. It returns False if the amount is less than the balance of the budget category and returns True otherwise. This method is used by both the withdraw method and transfer method.
When the budget object is printed it displays:

A title line of 30 characters where the name of the category is centered in a line of * characters.
A list of the items in the ledger. Each line shows the description and amount. The first 23 characters of the description is displayed, then the amount. The amount is right aligned, contain two decimal places, and display a maximum of 7 characters.
A line displaying the category total.
Here is an example of the output:

*************Food*************
initial deposit        1000.00
groceries               -10.15
restaurant and more foo -15.89
Transfer to Clothing    -50.00
Total: 923.96
Besides the Category class, a function (ouside of the class) called create_spend_chart takes a list of categories as an argument. It returns a string that is a bar chart.

The chart shows the percentage spent in each category passed in to the function. The percentage spent is calculated only with withdrawals and not with deposits. Down the left side of the chart is labels 0 - 100. The "bars" in the bar chart is made out of the "o" character. The height of each bar is rounded down to the nearest 10. The horizontal line below the bars goes two spaces past the final bar. Each category name is vertacally below the bar. There is a title at the top that says "Percentage spent by category".

This function can be tested with up to four categories.

Look at the example output below.

Percentage spent by category
100|          
 90|          
 80|          
 70|          
 60| o        
 50| o        
 40| o        
 30| o        
 20| o  o     
 10| o  o  o  
  0| o  o  o  
    ----------
     F  C  A  
     o  l  u  
     o  o  t  
     d  t  o  
        h     
        i     
        n     
        g     
The unit tests for this project are in test_module.py.

Development

Write your code in budget.py. For development, you can use main.py to test your Category class. Click the "run" button and main.py will run.

Testing

We imported the tests from test_module.py to main.py for your convenience. The tests will run automatically whenever you hit the "run" button.
