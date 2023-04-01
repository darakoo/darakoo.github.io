* Early return, early exit
  - 조건이 맞지 않는 로직은 앞에서 조건문으로 return 하고 
  - 조건에 맞는 로직은 조건절 밖에서 기술하는 것을 추천한다.

```
// bad
function upgradeUser(user){
  if(user.poing > 10){
    long upgrade logic...
  }
}

// good
function upgradeUser(user){
  if(user.poing <= 10){
    return;
  }
  
  long upgrade logic...
}
``
 
