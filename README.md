//call
var obj1={
    num:2
    
};
var obj2={
    f1:function(a,b,c){
        console.log(this.num+a+b+c);
    }
};
obj2.f1.call(obj1,2,"hello","world");
//meaning of call method The call() method is a predefined JavaScript method. It can be used to invoke (call) a method with an owner object as an argument (parameter). With call() , an object can use a method belonging to another object.

//apply
var obj1={
    num:2
    
};
var obj2={
    f1:function(a,b,c){
        console.log(this.num+a+b+c);
    }
};
var arr=[2,"hello","world"]
obj2.f1.apply(obj1,arr);
// meaning of apply() method With apply , you can write a method once, and then inherit it in another object, without having to rewrite the method for the new object. apply is very similar to call() , except for the type of arguments it supports. You use an arguments array instead of a list of arguments (parameters).

// bind()
var obj1={
    num:2
    
};
var obj2={
    f1:function(a,b,c){
        console.log(this.num+a+b+c);
    }
};
var r= obj2.f1.bind(obj1,2,"hello","world");
r();

// meaning of bind method bind() The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.




