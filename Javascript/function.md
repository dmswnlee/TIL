# ν¨μ(function)
π[poiemaweb](https://poiemaweb.com/) , λͺ¨λμλ°μ€ν¬λ¦½νΈ(deep dive)

<br>

## ν¨μλ?
* μλ ₯(input) λ°κ³  μΆλ ₯(output)μ λ΄λ³΄λ΄λ κ²
* λ΄λΆλ‘ μλ ₯λ°λ λ³μ : λ§€κ°λ³μ(parameter), μΈμ(argument)
* μΈλΆλ‘ μΆλ ₯νλ κ² : λ°νκ°(return)
* ν¨μλ **ν¨μμ μ**λ₯Ό ν΅ν΄ μμ±νκ³  μΈμλ₯Ό μ λ¬νμ¬ **ν¨μνΈμΆ**μ νκ³  κ²°κ³Όκ°μ **λ°ν**ν¨
* ν¨μλ λ°λ³΅λλ μΌμ μ€νν  λ μ μν΄λκ³  μ¬μ¬μ© ν¨
* ν¨μλ κ°μ²΄νμμ΄λ€. (λ³΅ν©λ°μ΄ν°)

<br>

### μΌκΈκ°μ²΄ 
μΌκΈκ°μ²΄μ μ‘°κ±΄
* λ¬΄λͺ λ¦¬ν°λ΄λ‘ μμ±κ°λ₯
* λ³μμ μ μ₯ κ°λ₯
* ν¨μμ λ§€κ°λ³μμ μ λ¬κ°λ₯
* ν¨μμ λ°νκ°μΌλ‘ μ¬μ© 

### μΌκΈν¨μ
* μλ°μ€ν¬λ¦½νΈμ ν¨μλ μΌκΈκ°μ²΄μ μ‘°κ±΄μ λ§μ‘±νλ―λ‘ μΌκΈκ°μ²΄, μΌκΈν¨μλΌκ³ λ νλ€.
* ν¨μκ°μ²΄λ νΈμΆν  μ μμ
* ν¨μ κ³ μ μ νλ‘νΌν°λ₯Ό κ°μ§ 

<br>

## ν¨μμ μ

<br>

### ν¨μμ μΈλ¬Έ
```js
    function ν¨μλͺ(λ§€κ°λ³μ) {
        return μ€νλ¬Έ
    }

    // ν¨μνΈμΈ
    ν¨μλͺ(μΈμ)
```

<br>

### ν¨μννμ
```js
    const λ³μλͺ = function(λ§€κ°λ³μ){
        return μ€νλ¬Έ
    }
```
* ν¨μμ΄λ¦μ μλ΅ν  μ μμ΄ **μ΅λͺν¨μ** λΌκ³ λ ν¨

<br>

### ν¨μνΈμ΄μ€ν(function hoisting)
* ν¨μννμκ³Ό λ¬λ¦¬ ν¨μμ μΈλ¬Έμ λ°νμμ΄μ μ μμλκΈ° λλ¬Έμ λ¨Όμ  μ€νλ¨
* ν¨μμ μΈλ¬Έ μ΄μ μ νΈμΆν΄λ νΈμΆλλ κ²
* μ½λμ μ λλ‘ λμ΄ μ¬λ €μ§κ²μ²λΌ λμνλ κ²μ νΈμ΄μ€νμ΄λΌκ³  ν¨

<br>

### νμ΄νν¨μ
```js
    const ν¨μλͺ = (λ§€κ°λ³μ) => μ€νλ¬Έ;
```
* es6
* ν¨μλ₯Ό λ κ°λ΅νκ² μ¬μ©κ°λ₯ 

<br>

## μ½λ°±ν¨μ 
```js
    function doubleScore(a, f) {
        for(let i=0; i<a; i++>){
            f(i);
        }
    };

    const double = function (i) {
        console.log(i * 2)
    }

    //νΈμΆ
    doubleScore(5, double) // 0, 2, 4, 6, 8
```
* λ§€κ°λ³μλ‘ κ°μ΄ μλ ν¨μλ₯Ό μ λ¬νλ κ²
* λ³μλ₯Ό ν΅ν΄ ν¨μ μΈλΆμμ μ½λ°±ν¨μλ₯Ό μ λ¬λ°μ ν¨μλ₯Ό **κ³ μ°¨ν¨μ**λΌκ³  ν¨

<br>

π ν¨μλ κ°μ²΄λ‘ μ°Έμ‘°μ μν λ°©μμΌλ‘ μ€νλλ€. μ΄λ ν¨μ λ΄λΆμμ μ¬μ©νλ μ§μ­λ³μμ κ°μ λ³κ²½νλ©΄ μΈλΆμ μλ μ μ­λ³μμ κ°λ λ³κ²½λκΈ° λλ¬Έμ λ³κ²½νμ§ μλ λΆλ³μ±μ μ μ§νλκ²μ΄ μ’λ€. 






