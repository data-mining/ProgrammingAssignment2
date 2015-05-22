source()
1. create a square matrix
> seq1 <- seq(1:4)
> m1 <- matrix(seq1,2)
> m1
     [,1] [,2]
[1,]    1    3
[2,]    2    4

2. create a cacheable matrix
> cm1 <- makeCacheMatrix(m1)

3. fetch the inverse matrix from cache
> im1 <- cacheSolve(cm1)
> im1
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5

4. verify if result is correct
> im2 <- solve(m1)
> im2
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5
> 
