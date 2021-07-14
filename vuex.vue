vue devtools for chrome extension 
fundamentals of vuex 
    DTO ya emit diyor 
props: are custom attributes you can register on a component. when a value is passed to a prop attribute, it becomes a property on that component instance 
events are used for communication between components as opposed to communication between DOM nodes. 
vue components makes dispatch to backend API(actions) -> actions commits mutation->mutations mutate state->state renders vue components
actions can be async 
mutations can only be sync 
getters is cached 
1st we create store instance
const store = new Vuex.Store({
    state: {},
    actions: {},
    getter:{},
    mutations: {}
})
2.state&getter





vuex+vue(SFC)
vuex+vue router
composing vuex 
vuex modules 
vuex plugins 
normalizing state 

