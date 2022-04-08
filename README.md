# Analizar-y-documenta-Scripts
# Script 1

    $number = 1 //Crea una variable number y le asigna un valor de 1

    Write-Host "The number is: " $number //Inprime la variable por pantalla

    $number = 2 //Sobrescribe la variable number y le asigna el valor 2

    Write-Host "The number is: " $number //Nuevamente imprime por pantalla la variable

    $number = 3 //Se vuelve a sobrescribir la variable number

    Write-Host "The number is: " $number //Se vuelve a imprimir por pantalla la misma variable

    $number = 4 //Se vuelve a sobrescribir la variable number

    Write-Host "The number is: " $number //Se imprime por ultima vez la variable
  
# Script 2

    // Cada vez que se completa el bucle, el código entre paréntesis se ejecutará mientras $counter sea menor que $repeat.
    // Cada vez que se completa el bucle, los símbolos ++ le indican a la variable que aumente en uno cada vez.
    [int]$repeat = 5

    for ($counter = 0; $counter -lt $repeat; $counter++) {
        Write-Host "hello"
    } 

    //El bucle while continuará hasta que $contador sea menor que (-lt) el valor 5 contenido en la variable $repeat.
    [int]$repeat = 5
    [int]$counter = 0

    while ($counter -lt $repeat) {
        Write-Host "hello"
        $counter++
    }

    //Do While Loop es una variante del bucle while, excepto que el código se ejecuta antes de verificar la condición para ver si se repite.
    [int]$repeat = 5
    [int]$counter = 0
    do {
        Write-Host "hello"
        $counter++
    }
    while ($counter -lt $repeat) 

    // Para cada bucle
    // Cada vez que se completa el bucle, la variable $character se convierte en el siguiente carácter de la lista hasta que no quedan caracteres.
    [string]$stringOfCharacters = "PowerShell for Beginners"

    foreach ($character in $stringOfCharacters.ToCharArray()) {
        Write-Host $character
    } 

    // Para cada bucle
    [string]$stringOfCharacters = "PowerShell for Beginners"
    $stringOfCharacters.ToCharArray() | ForEach-Object { Write-Host "$_" }

# Script 3
    if (4 -eq 4) {
        Write-Host "4 is equal to 4"
    }

    if ("hello" -eq "hello") {
        Write-Host "Both strings are equal to each other"
    } 

    [int]$x = 10
    [int]$y = 10

    if ($x -eq $y) {
        Write-Host "the x and y variables are equal to each other"
    }
    else {
        Write-Host "The x and y variables are NOT equal to each other"
    }

    $yourName = "Ian"

    if ($yourName -eq "Ian") {
        Write-Host "Hay my name is Ian too!"
    }
    else {
        Write-Host "Hi $yourName, nice to meet you!"
    }

    [string]$playerInput = ""

    $playerInput = Read-Host -Prompt "You walk into a room with two doorways. One to the left and one to the right. Type 'left' or 'Right' to walk through one of the doors."

    if ($playerInput -eq "left") {
        Write-Host "Player typed left"
    }
    elseif ($playerInput -eq "right") {
        Write-Host "Player typed right"
    }
    else {
        Write-Host "Player typed something we didn't understand"
    }

    if (5 -eq 5) {
        #5 is equal to 5
    }

    if (3 -ne 4) {
        #3 is not equal to 4
    }

    if (4 -gt 2) {
        #4 is greater than 2
    }

    if (2 -ge 1) {
        #2 is greater than or equal to 1
    }

    if (1 -lt 2) {
        #1 is less than 1
    }

    if (1 -le 2) {
        #1 is less than or equal to 2
    } 

    if ("hello how are you?" -like "hello*") {
        #use a wildcard character * to match strings
    }

    if ("HELLO" -notlike "BYE") {
        #HELLO is not like BYE
    } 

    if ("HELLO" -match "H") {
        #H exists in the 
        string "HELLO"
    }

    if ("HELLO" -notmatch "A") {
        #A does not match in the 
        string "HELLO"
    }

    $list = @(1, 2, 3, 4, 5)
    if ($list -contains 3) {
        #the list does contain a 3
    }

    $list = @(1, 2, 3, 4, 5)
    if ($list -notcontains 8) {
        #$list does not contain 8
    }

    $list = @(1, 2, 3, 4, 5)
    if (3 -in $list) {
        #the list does contain a 3
    } 

    $list = @(1, 2, 3, 4, 5)
    if (6 -notin $list) {
        #6 is not in the list
    }

    $var = "This is a string"
    if ($var -is [string]) {
        #The variable is a string
    }

    $var = "This is a string"
    if ($var -isnot [bool]) {
        #The variable is a string and not a Boolean value so results in true.
    } 

    [int]$number = 2
    switch ($number) {
        1 { "The number is one" }
        2 { "The number is two" }
        default { "I dont know what the number is" }
    }

    [string]$favouriteColour = "Blue"
    switch ($favouriteColour) {
        "Red" {
            "Your favourite colour is Red"
            "I like red too."
        }

        "Blue" {
            "Your favourite colour is Blue"
            "I like Blue too."
        }

        default { "I dont recognise that colour" }
    }
    
   # Explicacion
   El primer condicional comparara si 4 es equivalente a 4. Al ser true, reproduce el Write-Host e imprime que "4 es lo mismo que 4".

   El segundo condicional compara strings. En este caso compara si el string "Hello" es lo mismo que "Hello". Al ser true, usa otra vez el Write-Host con el mensaje      "Ambos strings son iguales"

   El tercer condicional es un if-else. Si las variables x e y son iguales, dará un mensaje, y si no lo son, el else actuará.

   El cuarto condicional conpara la variable yourName y tiene un if que compara la variable yourName con "Ian". Si es igual, imprimirá un mensaje. Si no lo es, el else    imprimirá el mensaje alternativo.
