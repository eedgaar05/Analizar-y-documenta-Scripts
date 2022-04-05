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

    # Cada vez que se completa el bucle, el código entre paréntesis se ejecutará mientras $counter sea menor que $repeat.
    # Cada vez que se completa el bucle, los símbolos ++ le indican a la variable que aumente en uno cada vez.
    [int]$repeat = 5

    for ($counter = 0; $counter -lt $repeat; $counter++) {
        Write-Host "hello"
    } 

    #El bucle while continuará hasta que $contador sea menor que (-lt) el valor 5 contenido en la variable $repeat.
    [int]$repeat = 5
    [int]$counter = 0

    while ($counter -lt $repeat) {
        Write-Host "hello"
        $counter++
    }

    #Do While Loop es una variante del bucle while, excepto que el código se ejecuta antes de verificar la condición para ver si se repite.
    [int]$repeat = 5
    [int]$counter = 0
    do {
        Write-Host "hello"
        $counter++
    }
    while ($counter -lt $repeat) 

    # Para cada bucle
    # Cada vez que se completa el bucle, la variable $character se convierte en el siguiente carácter de la lista hasta que no quedan caracteres.
    [string]$stringOfCharacters = "PowerShell for Beginners"

    foreach ($character in $stringOfCharacters.ToCharArray()) {
        Write-Host $character
    } 

    # Para cada bucle
    [string]$stringOfCharacters = "PowerShell for Beginners"
    $stringOfCharacters.ToCharArray() | ForEach-Object { Write-Host "$_" }
