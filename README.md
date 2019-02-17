# apktool-res-fix

1. 对apktool进行了修改,反编译资源xml时,通过 ***resource id***进行查找，而不是通过***String Name***进行查找。   
2. 对于某些使用了[AndResGuard](https://github.com/shwenzhang/AndResGuard)的app(如某信）, 直接使用原版apktool进行反编译，会出现如下错误:  

    > Could not decode file, replacing by FALSE value: xxxxxx
    
    使用这个版本的apktool则不会有这个错误    
3. 当然，apktool 也有不反编译资源的选项:
> -r,--no-res             Do not decode resources.

    如果不需要修改资源，使用这个选项也可
