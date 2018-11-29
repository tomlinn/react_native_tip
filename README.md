# react_native_tip

## 1 

``` java
onAddArray = () => {
  this.state.peo.unshift({ key: 1 });
};
```
it can be
``` java
const { peo } = this.state;
onAddArray = () => {
  peo.unshift({ key: 1 });
};
```

## 2

this will be error because it will be regnize as a string.
```java 
this.state = {
  money :'000'
}

onAddArray =() =>{
  var s=this.state.money;
  
  for(var i=0;i<num;i++){
    if(x!=i){
              a[i][x]+=s;
    }
  }
}
```
this will be corrent
```java 
this.state = {
  method :'0'
}

onAddArray =() =>{
  var s=this.state.money/1;
}
```


## 3
this will be warning and show the error of ``` text each child in an array or iterator should have a unique key prop```.<br>
it still can work but always show warning. it's annoying!
``` java
const a_input = a.map((type)=> <TextInput placeholder={type+""} />);

```

the reason is it will re-render the whole row because it can't not idefinty which should be re-rendor.<br>
So add the key, it should won't showing warning.<br>
[Fixed code]

``` java
const a_input = a.map((type,index)=> <TextInput key={index} placeholder={type+""} />);

```















