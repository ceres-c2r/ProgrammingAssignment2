# Test Run

> mymat<-matrix(c(1,2,3,4),2,2)
> mymat
     [,1] [,2]
[1,]    1    3
[2,]    2    4
> mymat2<-makeCacheMatrix(mymat)
> 

# Run First Time
> cacheSolve(mymat2)
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5

# Run Again
> cacheSolve(mymat2)
getting cached inverse data
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5

# Run directly using solve to verify answer
> solve(mymat)
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5
> 

# Test with 3D matrix> mymat<-matrix(c(1,2,3,4,5,6,7,9,8),3,3)
> det(mymat)
[1] 9
> mymat<-matrix(c(1,2,3,4,5,6,7,8,9),3,3)
> det(mymat)
[1] 0
> mymat<-matrix(c(1,2,3,4,5,6,7,9,8),3,3)
> det(mymat)
[1] 9
> mymat3<-makeCacheMatrix(mymat)
> cacheSolve(mymat3)
           [,1]       [,2]       [,3]
[1,] -1.5555556  1.1111111  0.1111111
[2,]  1.2222222 -1.4444444  0.5555556
[3,] -0.3333333  0.6666667 -0.3333333
> cacheSolve(mymat3)
getting cached inverse data
           [,1]       [,2]       [,3]
[1,] -1.5555556  1.1111111  0.1111111
[2,]  1.2222222 -1.4444444  0.5555556
[3,] -0.3333333  0.6666667 -0.3333333
> 

