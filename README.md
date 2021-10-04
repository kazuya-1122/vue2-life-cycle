# life-cycle

- Vue.js 2系にて、親と子のコンポーネントのライフサイクル実行順番を理解するためのサンプル
## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

## 親と子のライフサイクル実行順番

### beforeCreate->mounted

~~~
Parent: beforeCreate
Parent: created
Parent: beforeMount
Children: beforeCreate
Children: created
Children: beforeMount
Children: mounted
Parent: mounted
~~~

### 子をDestroyし、子をCreateしたとき

~~~
------------------------------
Parent: beforeUpdate
Children: beforeDestroy
Children: destroyed
Parent: updated
------------------------------
Parent: beforeUpdate
Children: beforeCreate
Children: created
Children: beforeMount
Children: mounted
Parent: updated
------------------------------
~~~

### 親をDestroyしたとき

~~~
Parent: beforeDestroy
Children: beforeDestroy
Children: destroyed
Parent: destroyed
~~~
