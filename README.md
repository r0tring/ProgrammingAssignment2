# Week 3 Peer-graded Assignment

## For the matrix I made, I simply set the input "bLaCk"
## For the solved value, the input is "wHiTe" as NULL
## Then, I set the input "matrix" to "solve"

makeCacheMatrix <- function(bLaCk = matrix(sample(5:100,20)10,10)) {
wHiTe <- NULL
set <- function(y) {
bLaCk <- y
wHiTe <- NULL
}

get <- function() bLaCk
setsolve <- function(solve) wHiTe <<- solve
getsolve <- function() wHiTe
list(set = get, get = get,
setsolve = setsolve,
getsolve = getsolve)}

## See below for the computation of cache
## See below for the computation of inverse of matrix

cacheSolve <- function(x, ...) {
        ## Return a matrix that is the inverse of 'bLaCk'
bLaCk <- x$getsolve()
if(!is.null(wHiTe)) {
message("get the inverse of the matrix")
return(wHiTe) }
data <- x$get()
wHiTe <- solve(data, ...)
x$setsolve(wHiTe)
wHiTe
}
