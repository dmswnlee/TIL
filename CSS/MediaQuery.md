# Media Query
📌 [김버그의css는재밌다](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

* Responsive web 반응형 웹을 만들기 위해서 반드시 알아야하는 css 선언

<br>

반응형 웹을 만들기 위해서는 반드시 2가지 요건이 충족되어야 함

```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width" />
		...
  </head>
</html>
```
```css
@media screen and (min-width:768px) {
    /* css 선언 */
}
```

* min-width
* max-width
