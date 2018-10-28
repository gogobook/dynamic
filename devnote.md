## 在vuetify 的`data-table` 是可叫出`v-dialog` 進行每一行的編輯的。
但細看才知這很厲害！

## 踩雷
vuetify.js 中 `import Vuetify from 'vuetify'`原本有`\lib` 要去掉否則無法正常顯示。

## 完成

原本`td` 之父元素是自動加上去的，改為手動加上，並且將`@click="editItem(props.item)"` 放置
於此即可完成個別行的觸發。

## 把props 的資料送到data 中。
https://stackoverflow.com/questions/45022705/vue-js-passing-props-to-data

使用watch
```js
watch: {
  comments(value) {
    this.allComments = value;
  }
}
```
這其實滿困難的，弄了很久才搞定。

## 自定義事件-關於emit 的使用。

https://cn.vuejs.org/v2/guide/components-custom-events.html
https://cn.vuejs.org/v2/guide/components.html#通过事件向父级组件发送消息