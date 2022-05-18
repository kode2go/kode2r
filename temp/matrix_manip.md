# Use stdout as per normal...
print("Question 1")

is.square <- function(M) {

var <- typeof(M)
print(var)

numrow <- nrow(M)
print(paste(numrow, "is number of rows"))
numcol <- ncol(M)
print(paste(numcol, "is number of rows"))
print("is.square function")
sprintf("%d is integer", numrow)
if(var == "integer")
{
    if(numrow == numcol){
    print("TRUE")
    } else {
    print("FALSE")
    }
     } 
}

a = 2

#var <- typeof(a)
#print(var)
is.square(a)

A = matrix(1:4,nrow=2,ncol=2)
is.square(A)

B = matrix(1:9,nrow=3,ncol=3)
is.square(B)

C = matrix(1:6,nrow=3,ncol=2)
is.square(C)   






