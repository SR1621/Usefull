String is immutable 
sringuffer is mutable and synchrozation 
stringbuild is not not synchrozation 
final is keywork 
finally is finally execution of the code 
Finalzie is to clear up the resource before garbase collector 

P1 obj=new P1() //it will shore in heap
stack is used by only  1 thread 

Arraylis is not syncrhosxed but vector is synchroied 

Arraylis is fast as compared to vector 
it increase the array size by 50% Vector define the incremetn size 
Array list use the iterator for traversing an array list 
***********
Hasmpa is not synschronzed where hashtable is syncronized 
Hashmap allows only null key and multiple null values 
hashtable doesn't allow any null key or value 
hashmap is fast as compared to hashtable 

equals and == Operator 
equals need to compare the values  and == is for numbers 

Lamda expresison syntax () -> {
}

Abstract vs interfaces 
*******************
Run time polymorshim -when we oover ride from the mail class is called run time polymorphism 
we can create  a abstract class and abstrac method and it can be overwridden in mail class 
we can create an interface and method and this can be implemeted from sub class and need to run by sub class method 
Abastract class will create an object but not interface
abstract class are faster not from interfaces 
*******************
overloaded method is compile time and override is runtime 
overload example 
int add(int a,int b)
double add(double a,double b)
we can't override static or private method in a class
static method of parent class will hiding in sub class -hiding concept  
multiple inheartance is not supported in java 
Cohesion is used to create a seperate class for each interface and can be invoked by different method 
encapsulation is hiding the implemnetation details 

set doesn;t allow dupllcaiton 
list allows duplication 
list add the specififc position or delete 
Queue order of processing 
map having key and vlaue 



anonymous function example 
lamda expression can be applied functioan interface 

it can contain only abstract method 
it is called functioan interace 
Runnable -run 
callable call 
comparable -compareTo 
cpmarator -compare
@FunciionInterface
void m1() 
defaul void m2() 
() -> { } Syntax method
****************************
Consumer ---we don't want to return any thing 
void accept(T) 
andThen
***************
Preicate 
Condition statment we can use preidcate 
boolean Test(T t)

************************* 
Supplierl interface 
T get();
no input and except as return type 
*********************
function 
*****************
apply() //which it takes as input parameter and return as output parameter  

****************************************************************************
A Stream API is used to process collection of objects
A Steam is a sequence of objects that supports various methods which can be pipelined to produce the desired result 
A Steam is not a data structure insted it takes input from the collection,Arays or I/O channels.
Steams don't change the orginal data strucute ,they only provide the result as per the pipelined methods 
*************
We can achieve fucntion programing 
code reduce 
Bulk operation 

****************
Filter for conditon  if and else 
For each for iteration 
**************

map() and flatMap()  widely used in Java streams 
these method are intermediat method and return stream as part of output 
map() method used for transformation 
flatMap used for transformation and flattering
flatMap() -- > Map + Flattering 

******************
Map() takes stream T as input and reutrn Stream as output 
One to one mapping 

flatMap() --takes stream as steam as input and returns as stream as output 
One to Many mapping 
Stream.of("A","B)

a,b
flatmap contains stream of sream and provides single output 

************************
Optional 
static method are available 
for ex :empty 
of
ofNullable
static mehthods
filter
flatMap
map
get
ifPresent
isPresent
orelse
orelseGet
orElseThrow

Interface can contain asbstrac methods
void draw();
default void area() 
{
}
static methods() 
}
default method can be overwriden but static methods can't override in the implemenation classes

******************************
Map and Reduce 
Map---Transferring data
Reduce --to aggregating data 

reduce(T Identiy ,BinaryOperator<T> accumlator)

accumlator is where we are calculating the function 

collection 
**********
List 
******
ArrayList 
ListLikedList 

*********set 
hasset 
LinkedHashSet
TreeSet
**************
Map 
HashTable


List will allow the duplciate vlaues and set doesn't all duplicate values
List work on index base and set on Hash Code 
ArrayList is backed by an Array while HashSet is backed by an HashMap

ArrayList and LinkedList 

ArrayList internally uses a dynamic array to store the elemetns  --LinkedList uses a doubly linked list to store the elemetns 

Manipulation the allarylist is slow  --manipulation with linkedlist is faster 

ArrayList is better for sorting and accesing 

ArrayList arrayList=new ArrayLust<string>();
List<String> list=mew ArrayList<>(); 


CustArrayList extendds ArrayList 
bolean add (Object 0 )
{
if(this.contaions o)
return true 
}else return super.add(o)


if we are implemention custoobject for set we need to hashcode and equals method 
if not it allows duplication value but not in the primitie types 
*********************
comparable and comparator 
*********************

comprable --single sorint and comparator --multiple 

compareTo() and compare() 
java.lang and java.util package 

Hashtable locks whole table ,but when it comes concurrenthashmap it locks only specific field 

    public static List<Customer> getAll() {
        return Stream.of(
                new Customer(101, "john", "john@gmail.com", Arrays.asList("397937955", "21654725")),
                new Customer(102, "smith", "smith@gmail.com", Arrays.asList("89563865", "2487238947")),
                new Customer(103, "peter", "peter@gmail.com", Arrays.asList("38946328654", "3286487236")),
                new Customer(104, "kely", "kely@gmail.com", Arrays.asList("389246829364", "948609467"))
        ).collect(Collectors.toList());
    }

 List<String> emails = customers.stream()
                .map(customer -> customer.getEmail())
                .collect(Collectors.toList());
        System.out.println(emails);

Exa :Flat Map
     List<String> phones = customers.stream()
                .flatMap(customer -> customer.getPhoneNumbers().stream())
                .collect(Collectors.toList());
        System.out.println(phones);
		
****************
reduce  --aggreagading data 
    Integer maxvalue = numbers.stream().reduce(0, (a, b) -> a > b ? a : b);
        System.out.println(maxvalue);
		
		  double sumSalary = EmployeeDatabase.getEmployees().stream()
                .filter(employee -> employee.getGrade().equalsIgnoreCase("A"))
                .map(employee -> employee.getSalary())
                .mapToDouble(i -> i)
                .sum();




 Java 17 
 indent --moving the space of a string 
 transform --new string builder 
 SWITCH Expression 
 text 
 instanceOf
 Records
 Sealed Classes
 