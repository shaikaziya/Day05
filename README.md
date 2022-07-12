# DAY-05

# 1.a)Print odd numbers in an array
# anonymous function:-

var arr=function(array){\
for(var i=0;i<array.length;i++){\
if(array[i]%3==0){\
console.log(array[i])}\
}\
}\
arr([1,2,3,4,5,6,7,8,9,10])


# IIFE:-

(function odd(array){\
for(var i=0;i<array.length;i++){\
if(array[i]%3==0){\
console.log(array[i])\
}\
}\
}([1,2,3,4,5,6,7,8,9,10]))


# 1.b)Convert all the strings to title caps in a string array
# anonymous function:-

var arrayElements=function titleCase(array){\
array1=[]\
for(var i=0;i<array.length;i++){\
   var y=array[i].charAt(0).toUpperCase()\
    var x=array[i].slice(1)\
    var z=y+x\
    array1.push(z)\
}\
console.log(array1)\
}\
arrayElements(["apple","banana","cat"])


# IIFE:-

(function titleCase(array){\
array1=[]\
for(var i=0;i<array.length;i++){\
   var y=array[i].charAt(0).toUpperCase()\
    var x=array[i].slice(1)\
    var z=y+x\
    array1.push(z)\
}\
console.log(array1)\
})(["apple","banana","cat"])


# 1.c)Sum of all numbers in an array
# anonymous function:-

var arr=function(array){\
var sum=0;\
for(var i=0;i<array.length;i++){\
sum=sum+array[i]\
}\
console.log(sum)\
}\
arr([1,2,3,4,5,6,7,8,9,10])


# IIFE:-

(function sumValue(array){\
var sum=0;\
for(var i=0;i<array.length;i++){\
sum=sum+array[i]\
}\
console.log(sum)\
})([1,2,3,4,5,6,7,8,9,10])



# 1.d)Return all the prime numbers in an array

  let arr= [-1,-2,-3,1,2,3,4,5,6,7,8,9,10];\
   let result = [];\
   function isPrime(arr) {\
   if(arr< 2) return false;\
   for (let k = 2; k < arr; k++){\
     if(arr % k == 0){\
       return false;\
     }\
        }\
     return true;\
    }\
      arr.forEach(function (element) {\
      const item = isPrime(element);\
     if (item) {\
     result.push(element);\
       }\
     });\
     console.log(result);


# 1.e)Return all the palindromes in an array
# anonymous function:-

var array1=[]\
var palindromeArray=function palindrome(array){\
for(var i=0;i<array.length;i++){\
var value=array[i].split("")\
if(array[i]==value.reverse().join("")){\
array1.push(array[i])\
}\
}\
}\
palindromeArray(["civic","hello","madam","aziya"])\
console.log(array1)


# IIFE:-

(function palindrome(array){

var array1=[]\
for(var i=0;i<array.length;i++){\
var value=array[i].split("")\
if(array[i]==value.reverse().join("")){\
array1.push(array[i])\
}\
}\
console.log(array1)\
})(["civic","hello","madam","aziya"])


# 1.f)Return median of two sorted arrays of the same size

{\
let j = 0;\
let i = n - 1;\
while (ar1[i] > ar2[j] && j < n && i > -1)\
{\
    let temp = ar1[i];\
    ar1[i] = ar2[j];\
    ar2[j] = temp;\
    i--; j++;\
}\
ar1.sort(function(a, b){return a - b});\
ar2.sort(function(a, b){return a - b});\
return parseInt((ar1[n - 1] + ar2[0]) / 2, 10);\
}\
let ar1 = [ 1, 12, 15, 26, 38 ];\
let ar2 = [ 2, 13, 17, 30, 45 ];\
let n1 = 5;\
let n2 = 5;\
if (n1 == n2)
console.log(getMedian(ar1, ar2, n1));\
else\
console.log("Doesn't work for arrays of unequal size");


# 1.g)Remove duplicates from an array
# anonymous function:-

var dulicateRemoved=function removeDuplicates(array){\
var arr1=[]\
for(var i=0;i<array.length;i++){\
if(arr1.indexOf(array[i])===-1){\
arr1.push(array[i])\
}\
}\
console.log(arr1)\
}\
dulicateRemoved([1,2,3,1,3,7,8])

# IIFE:-

(function removeDuplicates(array){\
var arr1=[]\
for(var i=0;i<array.length;i++){\
if(arr1.indexOf(array[i])===-1){\
arr1.push(array[i])\
}\
}\
console.log(arr1)\
})([1,2,3,1,3,7,8])



# 1.h)Rotate an array by k times

function arrayRotate(arr, k) {\
      k -= arr.length * Math.floor(k / arr.length);\
      arr.push.apply(arr, arr.splice(0, k));\
      return arr;\
   }\
  for(let i =0 ; i <= 3 ; i++) {\
  console.log(arrayRotate(["Guvian","a","am","I"], i), i);\
  }


# 3.a)Print odd numbers in an array

var array=(arr)=>{\
for(var i=0;i<arr.length;i++){\
if(arr[i]%3==0){\
console.log(arr[i])}\
}\
}\
array([1,2,3,4,5,6,7,8,9,10])


# 3.b)Convert all the strings to title caps in a string array

var arrayElements=(array)=>{\
array1=[]\
for(var i=0;i<array.length;i++){\
   var y=array[i].charAt(0).toUpperCase()\
    var x=array[i].slice(1)\
    var z=y+x\
    array1.push(z)\
}\
console.log(array1)\
}\
arrayElements(["apple","banana","cat"])


# 3.c)Sum of all numbers in an array

var arr=(array)=>{\
var sum=0;\
for(var i=0;i<array.length;i++){\
sum=sum+array[i]\
}\
console.log(sum)\
}\
arr([1,2,3,4,5,6,7,8,9,10])


# 3.d)Return all the prime numbers in an array

   var arr=[26,2,3,5,77,88,93,71,31];\
   var primenum=num=>{\
      for (var i=2;i<num;i++){\
         if(num%i===0)  return false;\
      }\
     return num !== 1;\
     };\
   var prime=arr.filter((ele)=>primenum(ele));\
    console.log(prime);


# 3.e)Return all the palindromes in an array

var array1=[]\
var palindromeArray=(array)=>{\
for(var i=0;i<array.length;i++){\
var value=array[i].split("")\
if(array[i]==value.reverse().join("")){\
array1.push(array[i])\
}\
}\
}\
palindromeArray(["civic","hello","madam","aziya"])\
console.log(array1)



