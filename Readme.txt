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
 


official CLI 
    npm install -g @vue/cli  or vue ui
vue create projectNAME
{{ doesnot work in html attribute }} so we use v-bind: or we just use :src for example 
conditionals 
    v-if v-else v-else-if v-show
    <template> tag ile tum container can be hide or shown 
v-model turnery operator gibi calisiyor,