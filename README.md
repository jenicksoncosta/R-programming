# R-programming
Coursera (R Programming)

## Armazenando o Inverso de uma Matriz em Cache: 
## Inversão de matriz é geralmente um cálculo caro e pode haver algum 
## benefício em armazenar em cache o inverso de uma matriz em vez de computá-lo repetidamente. 
## Abaixo está um par de funções que são usadas para criar um objeto especial que 
## armazena uma matriz e armazena em cache sua inversa.

## Esta função cria um objeto de "matriz" especial que pode armazenar em cache seu inverso.

makeCacheMatrix <- função ( x = matriz ()) {
         inv <- conjunto NULL <- função ( y ) {                 x << - y                 inv << - NULL         } get <- função () x         setInverse <- função ( inverso ) inv << - inverse         getInverse <- function () inv         list ( set = set , get = get
        



        



             , 
             setInverse = setInverse, 
             getInverse = getInverse) 
}


## Esta função calcula o inverso da "matriz" especial criada por 
## makeCacheMatrix acima. Se o inverso já foi calculado (e a 
matriz ## não mudou), ele deve recuperar o inverso do cache.

cacheSolve <- function ( x , ...) { ## Retorna uma matriz que é o inverso de 'x'         inv <- x $ getInverse () if (! is. null (inv)) {                 message ( "obtendo dados em cache " ) return (inv)         }         mat <- x $ get ()         inv <- solve (mat, ...)         x $ setInverse (inv)         inv }
        

        

                









