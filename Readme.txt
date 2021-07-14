vue devtools
vue devtools 3 beta 
vetur 
vue vs code snippets 
const App = {
    data(){
        return{
            message:"HelloWorld"
        }
    }
}
Vue.createApp(App).mount("#app")


in vue:
const App ={
    data(){
        return {
            items: [ 
                "a", "s", xxxxxxxxxxxxx
            ]
        }
    }
}
 htm l de ise v-for="item for items"> {{item}}
 some of directives:
 v-if, v-else , v-else*if, v-show, v-for, v-text, v-html, v-slot, v-on, v-bind, v-model, v-model, v-pre, v-cloak, v-once, v-is 
 v-model: creates a relationship between the data in the instance/component and a form input, so you can dynamically update values 
    v-model="message" setState in otomatigi textbox icin kullaniliyor genellile
v-if/v-show: is a conditional that will display information dependong on meeting a requirement. this can be anything-buttons, forms, divs, components
    disabled sarti gibi kullanilabilinit button i gizle goster veya template i 
    v-show ise true/false gibi kullaniliyor genellikle toggle value 
v-bind or :
    one of the most useful directives so there is a shortcut! we can use it for soo many things-class and style binding, creating dynamic props, etc..
v-for = loops through a set of values , can also do a static number 
v-once and v-pre = not quite as useful, v-once will NOT update once its beeen rendered
v-pre= will print out the inner text exactly how it is, including code(good for documentation)
 {{$NAME}} vue nin kendi variable i m bizim atadigimiz deger JSON.stringify() gibi dusun 
v-on or @
    Extremely useful so there is a shortcut v-on is great for binding to events like click and mouseenter. you ae able to pass in a parameter for the event like(e). we can also use ternaries directly 
    multiple bindigs can be 
v-html = great for strings  that have html elements that need to be rendered 
v-text = {{}} sembolun yerine gecer 
modifiers =
    v-model.trim gibi , it will strip any leading or trailing whitespace from the bound string 
    v-model.number changes strings to number inputes
    v-model.lazy wont populate the content automatically, it will wait to bind until an event happens.(it listens to change events instead of inputs)
    

official CLI 
    npm install -g @vue/cli  or vue ui
vue create projectNAME
{{ doesnot work in html attribute }} so we use v-bind: or we just use :src for example 
conditionals 
    v-if v-else v-else-if v-show
    <template> tag ile tum container can be hide or shown 
v-model turnery operator gibi calisiyor,
methods = are bound to the vue instance, they are incredibly useful for functions you would like to access in directives 
    vue de eventleri icin e parametrelerini gondermemize gerek yok 
methods in forms 
    methodlarda top level da arrow fuction kullanilmiyor yoksa this kayboluyor ama functionin icinde arrow kullanabiliyoruz 
computed = computed propertirs are calculations that will be cached and will only update when needed.
    highly performant but use with understanding
computed                                        methods
=========================================       ===========================================
runds only when a dependecys has changed        runs whenever an update occurs
cached                                          not cached
should be use d as a property,in place of        typically invoked from v-on/@, but flexible
    data                                        getter/ setter 
by default getter only, but you can define
    a setter
vue3 = FILTERs is difference ith vue2 
watchers and Reactive = Reactive programming is programming with asynchronous data streams 
proxies = An object that encases another object or function and allows you to intercept it. 
new Proxy(target, handler) // 2 function i birbirine baglar Reflect ile birlikte 
    Reflect Binds this properly //Proxies are wathing changes on value 
    Proxies are ES6 /(previously Object.defineProperty)
set() = A set is a series of any values, similar to an array, where any particular value can only be interested once.
map() = A Map is a series of keys and values, similar to an object, but with some differences
WeakMap() = similar to a MAP() but the references are held weakly, in other words, if you delete something, the reference can be garbage collected
watchers = good for asynchronous updates, and updates/transtions with data changes 
templates = 
vue.js uses html based template syntax to bind the vue instance to the DOM, very useful for components 
    templates are optional, you can also write render fuctions with optional jsx support 
components a collection of elements that are encapsulated into a group that can be accessed through one single element     
props = passing data from the parent to the child 
    not using the state of the parent 
        <child count="1"></child>
    using the state of the parent 
        <child :count="count"></child>
emits : child to parent
    Vuex and composition API 
    <button @click="$emit("gettaco")">click me to order taco</button>
        gettaco is special click event that we named
        @gettaco="updateTaco is method name"
    <my-component @myevent="parentHandler"></my-component>
    <button @click="$emit("myevent")"></button>
    <button @click="$emit("myevent", param)"></button> when we want to report parent element we use 2nd argument 
slots
    can help to show be default text , slot span gibi ama mesala ana componentin icerisinde bir baska componentin basligini yazdirmak gibi, nested components gibi dusun, child component te slot tagi icersinde yazilir parent componentte ise child component taginin icerisine yazilir 
keep alive :is=""
    it remembers which component is selected and where we are 
single file templates=
    <template>
        <div></div>
    </template>
    <script>
        //import libraries
        <export default {
            // write your vue component logic here 
            components: {

            }
        }
    </script>
    <style scoped>
        // write your styles for the component in here 
    </style>
    npm i -g @vue/cli 
    snippets save lifes 
        vue-vscode-snippets
        vetur for vscode 
    lifecycle hooks = also auto bind to the instance so that you can use the components state, and methods. for this reason you should not use Arrow function on lifecycle methods, as it will return to parent.
        beforeCreate
        created-great place to call API 
        beforeMount
        mounted-great place to work on DOM operations
        beforeUpdate 
        updated 
        activated - associated for keep-alive
        deactivated 
        beforeUnmount 
        unmounted 
        errorCaptured 
        renderTracked 
        renderTriggered
https://v3.vuejs.org/guide/instance.html#lifecycle-diagram 
why NUXT
    SSR/Static/Jamstack/SPA
    router is in builtin 
css transtions toggle , interpolate 2 state, but not creating loops 
animatons da loops yapiliyor 
transtition component 