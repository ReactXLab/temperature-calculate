[![license][license-image]][license-url]

# 溫度換算
[狀態提升練習]輸入攝氏(華氏)即可換算出華氏(攝氏)溫度


## Demo
[連結](https://reactxlab.github.io/temperature-calculate/)

<img src="./screenshot/img01.png">

* React在DOM原生組件`<input>`上調用指定的`onChange`函數。在本例中，指的是`TemperatureInput`組件上的`handleChange`函數。
* `TemperatureInput`組件的`handleChange`函數會在值發生變化時調用`this.props.onTemperatureChange()`函數。這些props屬性，像`onTemperatureChange`都是由父組件`Calculator`提供的。
* 當最開始渲染時，`Calculator`組件把內部的`handleCelsiusChange`方法指定給攝氏輸入組件`TemperatureInput`的`onTemperatureChange`方法，並且把`handleFahrenheitChange`方法指定給華氏輸入組件`TemperatureInput`的`onTemperatureChange` 。兩個`Calculator`內部的方法都會在相應輸入框被編輯時被調用。
* 在這些方法內部，`Calculator`組件會讓React使用編輯輸入的新值和當前輸入框的溫標來調用`this.setState()`方法來重渲染自身。 * React會調用`Calculator`組件的`render`方法來識別UI界面的樣子。基於當前溫度和溫標，兩個輸入框的值會被重新計算。溫度轉換就是在這裡被執行的。
* 接著React會使用`Calculator`指定的新props來分別調用`TemperatureInput`組件，React也會識別出子組件的UI界面。
* React DOM 會更新DOM來匹配對應的值。我們編輯的輸入框獲取新值，而另一個輸入框則更新經過轉換的溫度值。

## LICENSE
MIT


[license-image]: https://img.shields.io/badge/license-MIT-blue.svg
[license-url]: https://github.com/ReactXLab/temperature-calculate/blob/master/LICENSE
