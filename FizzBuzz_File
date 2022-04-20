#FizzBuzz
import numpy as np

def FizzBuzz(start, finish):
    index_arr=np.arange(start,finish+1)
    num_arr=np.array(index_arr,dtype="object")
    choice_list=[num_arr%15==0,num_arr%3==0,num_arr%5==0,num_arr==num_arr]
    char_list=['fizzbuzz','fizz','buzz',num_arr]
    
    output=np.select(choice_list,char_list)
    return(output)
