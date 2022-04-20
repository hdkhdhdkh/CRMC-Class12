#getBondprice

import numpy as np
import itertools as it

def getBondPrice(y, face, couponRate, m, ppy=1):
    y=y/ppy
    couponRate = couponRate/ppy
    coupon = face*couponRate
    m=m*ppy
    
    t=list(range(1,m+1))
    t_array=np.array(t)
    
    pv=np.array(list(it.repeat(1,m)))
    pv_array=pv*(y+1)**(-1*t_array)
    
    cf=list(it.repeat(coupon,m))
    cf[-1]=cf[-1]+face
    cf_array=np.array(cf)
    
    bondprice=sum(pv_array*cf_array)
    return(bondprice)
