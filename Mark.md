Vue 组件间通讯
1. props 和 $emit -- 父子组件间通信

2. provide 和 inject -- 父子组件、兄弟组件间通信

3. eventBus(实例化一个Vue对象), 通过 $on 和 $emit -- 父子组件、兄弟组件间通信
```
import Bus from '../eventBus.js'
Bus.$emit('data-input', data) -- 传输数据
Bus.$on('data-input', data => {}) -- 接收数据
```
// eventBus.js
```
import Vue from 'vue'
export default new Vue()
```

4. $parent 和 $children -- 父子组件间通信 (还有一个 ref 和 $refs )

5. vuex -- 父子组件、兄弟组件间通信

6. $attrs 和 $listeners -- 父子组件间通信

7. npm包 pubsub-js , 通过 publish 和 subscribe -- 父子组件、兄弟组件间通信
```
import PubSub from 'pubsub-js'
PubSub.publish('pubMessage', data) -- 传输数据
PubSub.subscribe('pubMessage', (event, data) => {}) -- 接收数据(注意：接收到的参数有两个, 第二个参数才是组件传输过来的参数)
```