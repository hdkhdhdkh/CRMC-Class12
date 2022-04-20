#BondDuration
import numpy as np
import itertools as it

def getBondDuration(y, face, couponRate, m, ppy=1):
    y=y/ppy
    couponRate = couponRate/ppy
    coupon = face*couponRate
    m=m*ppy
    
    t=list(range(1,m+1))
    t_array=np.array(t)
    t_array=t_array/ppy
    
    count=list(it.repeat(1,m))
    pv_array=(np.array(count)+y)**(-1*t_array)
    
    cf=list(it.repeat(coupon,m))
    cf[-1]=cf[-1]+face
    cf_array=np.array(cf)
    
    bondprice=sum(pv_array*cf_array)
    w_pvcf=sum(pv_array*cf_array*t_array)
    duration=w_pvcf/bondprice
    return(duration)
