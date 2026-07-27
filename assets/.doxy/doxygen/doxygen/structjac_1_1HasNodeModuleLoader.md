

# Struct jac::HasNodeModuleLoader

**template &lt;class Machine&gt;**



[**ClassList**](annotated.md) **>** [**jac**](namespacejac.md) **>** [**HasNodeModuleLoader**](structjac_1_1HasNodeModuleLoader.md)




























## Public Static Attributes

| Type | Name |
| ---: | :--- |
|  constexpr bool | [**value**](#variable-value)   = `std::is\_same\_v&lt;decltype(test&lt;Machine&gt;(std::declval&lt;Machine&&gt;())), std::true\_type&gt;`<br> |
















## Public Static Functions

| Type | Name |
| ---: | :--- |
|  auto | [**test**](#function-test-12) (T & m) <br> |
|  std::false\_type | [**test**](#function-test-22) (...) <br> |


























## Public Static Attributes Documentation




### variable value 

```C++
constexpr bool jac::HasNodeModuleLoader< Machine >::value;
```




<hr>
## Public Static Functions Documentation




### function test [1/2]

```C++
template<class T>
static auto jac::HasNodeModuleLoader::test (
    T & m
) 
```




<hr>



### function test [2/2]

```C++
template<class T>
static std::false_type jac::HasNodeModuleLoader::test (
    ...
) 
```




<hr>

------------------------------
The documentation for this class was generated from the following file `src/jac/device/device.h`

