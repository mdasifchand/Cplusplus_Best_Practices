
<HR>
<A name=names></A>
<H1>Names </H1>
<HR>
<A name=units></A>
<H2>Include Units in Names </H2>If a variable represents time, weight, or some 
other unit then include the unit in the name so developers can more easily spot 
problems. For example: <PRE>uint32 mTimeoutMsecs;
uint32 mMyWeightLbs;
</PRE>Better yet is to make a variable into a class so bad conversions can be 
caught.
  <hr>
<A name=classnames></A>
<H2>Class Names </H2>
<UL>
  <LI>Use upper case letters as word separators, lower case for the rest of a 
  word 
  <LI>First character in a name is upper case 
  <LI>No underbars ('_') </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>Of all the different naming strategies many people found this one the best 
  compromise. </LI></UL>
<H3>Example </H3><PRE>   class NameOneTwo
  
   class Name
  </PRE>
<P>
  <H3><B>Class Names</B> 
<H3></H3>
<UL>
  <LI>Name the class after what it is. If you can't think of what it is that is 
  a clue you have not thought through the design well enough. 
  <LI>Compound names of over three words are a clue your design may be confusing 
  various entities in your system. Revisit your design. Try a CRC card session 
  to see if your objects have more responsibilities than they should. 
  <LI>Avoid the temptation of bringing the name of the class a class derives 
  from into the derived class's name. A class should stand on its own. It 
  doesn't matter what it derives from. 
  <LI>Suffixes are sometimes helpful. For example, if your system uses agents 
  then naming something DownloadAgent conveys real information. </LI></UL>
<HR>
<A name=classlnames></A>
<H2>Class Library Names </H2>
<UL>
  <LI>Now that name spaces are becoming more widely implemented, name spaces 
  should be used to prevent class name conflicts among libraries from different 
  vendors and groups. 
  <LI>When not using name spaces, it's common to prevent class name clashes by 
  prefixing class names with a unique string. Two characters is sufficient, but 
  a longer length is fine. </LI>
  <LI> It is strongly recommended to use namespaces</li></UL>
<H3>Example </H3>John Johnson's complete data structure library could use 
<I>JJ</I> as a prefix, so classes would be: <PRE>   class JjLinkList
   {
   }
</PRE>
<P>
<HR>
<A name=methodsnames></A>
<H2>Method Names </H2>
<UL>
  <LI>Use the same rule as for class names. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>Of all the different naming strategies many people found this one the best 
  compromise. </LI></UL>
<H3>Example </H3><PRE>   class NameOneTwo
   {
   public:
      int                   DoIt();
      void                  HandleError();
   }
</PRE>
<P>
  <H3>Method Names </H3>
<UL>
  <LI>Usually every method and function performs an action, so the name should 
  make clear what it does: CheckForErrors() instead of ErrorCheck(), 
  DumpDataToFile() instead of DataFile(). This will also make functions and data 
  objects more distinguishable. 
  <P>Classes are often nouns. By making function names verbs and following other 
  naming conventions programs can be read more naturally. 
  <P></P>
  <LI>Suffixes are sometimes useful: 
  <UL>
    <LI><I>Max</I> - to mean the maximum value something can have. 
    <LI><I>Cnt</I> - the current count of a running count variable. 
    <LI><I>Key</I> - key value. </LI></UL>
  <P>For example: RetryMax to mean the maximum number of retries, RetryCnt to 
  mean the current retry count. 
  <P></P>
  <LI>Prefixes are sometimes useful: 
  <UL>
    <LI><I>Is</I> - to ask a question about something. Whenever someone sees 
    <I>Is</I> they will know it's a question. 
    <LI><I>Get</I> - get a value. 
    <LI><I>Set</I> - set a value. </LI></UL>
  <P>For example: IsHitRetryLimit. 
  <P></P></LI></UL>
<HR>
<A name=attrnames></A>
<H2>Class Attribute Names </H2>
<UL>
  <LI>Attribute names should be prepended with the character 'a'. 
  <LI>After the 'a' use the same rules as for class names. 
  <LI>'a' always precedes other name modifiers like 'p' for pointer. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>Prepending 'a' prevents any conflict with method names. Often your methods 
  and attribute names will be similar, especially for accessors. </LI></UL>
<H3>Example </H3><PRE>   class NameOneTwo
   {
   public:
      int                   VarAbc();
      int                   ErrorNumber();
   private:
      int                   aVarAbc;
      int                   aErrorNumber;
      String*               apName;
   }
</PRE>
<P>
<HR>
<A name=margnames></A>
<H2>Method Argument Names </H2>
<UL>
  <LI>The first character should be lower case. 
  <LI>All word beginnings after the first letter should be upper case as with 
  class names. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>You can always tell which variables are passed in variables. 
  <LI>You can use names similar to class names without conflicting with class 
  names. </LI></UL>
<H3>Example </H3><PRE>   class NameOneTwo
   {
   public:
      int                   StartYourEngines(
                               Engine&amp; rSomeEngine, 
                               Engine&amp; rAnotherEngine);
   }
</PRE>
  <P>
  <HR>
<A name=fext>
<H2>C++ File Extensions </H2>In short: Use the <I>.hh</I> extension for header 
files and <I>.cc</I> for source files. 

<P>
<HR>
 <A name=cnames></A>
<H2>C Function Names </H2>
<UL>
  <LI>In a C++ project there should be very few C functions. 
  <LI>For C functions use the GNU convention of all lower case letters with '_' 
  as the word delimiter. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>It makes C functions very different from any C++ related names. </LI></UL>
<H3>Example </H3><PRE>   int
   some_bloody_function() {
   }
</PRE>
  <hr>
  
  <A name=descriptive></A>
<H2>Make Names Fit </H2>Names are the heart of programming. In the past people 
believed knowing someone's true name gave them magical power over that person. 
If you can think up the true name for something, you give yourself and the 
people coming after power over the code. Don't laugh! 
<P>A name is the result of a long deep thought process about the ecology it 
lives in. Only a programmer who understands the system as a whole can create a 
name that "fits" with the system. If the name is appropriate everything fits 
together naturally, relationships are clear, meaning is derivable, and reasoning 
from common human expectations works as expected. 
<P>If you find all your names could be Thing and DoIt then you should probably 
revisit your design. 
<P>

<H3>No All Upper Case Abbreviations </H3>
<UL>
  <LI>When confronted with a situation where you could use an all upper case 
  abbreviation instead use an initial upper case letter followed by all lower 
  case letters. No matter what. </LI></UL>
<H4>Justification </H4>
<UL>
  <LI>People seem to have very different intuitions when making names containing 
  abbreviations. It's best to settle on one strategy so the names are absolutely 
  predictable. 
  <P>Take for example <I>NetworkABCKey</I>. Notice how the C from ABC and K from 
  key are confused. Some people don't mind this and others just hate it so 
  you'll find different policies in different code so you never know what to 
  call something. </P></LI></UL>
<H4>Example </H4><PRE>   class FluidOz             // NOT FluidOZ
   class NetworkAbcKey       // NOT NetworkABCKey
</PRE>
<P>

<HR>
<A name=stacknames></A>
<H2>Variable Names on the Stack </H2>
<UL>
  <LI>use all lower case letters 
  <LI>use '_' as the word separator. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>With this approach the scope of the variable is clear in the code. 
  <LI>Now all variables look different and are identifiable in the code. 
</LI></UL>
<H3>Example </H3><PRE>   int NameOneTwo::HandleError(int errorNumber) {
      int            error= OsErr();
      Time           time_of_error;
      ErrorProcessor error_processor;
   }
</PRE>
<P>
<HR>
<A name=pnames></A>
<H2>Pointer Variables </H2>
<UL>
  <LI>pointers should be prepended by a 'p' in most cases 
  <LI>place the <I>*</I> close to variable name not pointer type
</LI></UL>

<H3>Example </H3><PRE>  String *pName= new String;

  String *pName, name, address; // note, only pName is a pointer.
</PRE>
<P>
<HR>
<A name=rnames></A>
<H2>Reference Variables and Functions Returning References</H2>
<UL>
  <LI>References should be prepended with 'r'. </LI>
  <LI>Const refs should not have 'r'.</LI>
</UL>
<H3>Justification </H3>
<UL>
  <LI>The difference between variable types is clarified. 
  <LI>It establishes the difference between a method returning a modifiable 
  object and the same method name returning a non-modifiable object. </LI></UL>
<H3>Example </H3><PRE>   class Test
   {
   public:
      void               DoSomething(StatusInfo&amp; rStatus);

      StatusInfo&amp;        rStatus();
      const StatusInfo&amp;  Status() const;

   private:
      StatusInfo&amp;        arStatus;
   }
</PRE>
<P>
<HR>
<A name=gnames></A>
<H2>Global Variables </H2>
<UL>
  <LI>Global variables should be prepended with a 'g'. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>It's important to know the scope of a variable. </LI></UL>
<H3>Example </H3><PRE>    Logger  gLog;
    Logger* gpLog;
</PRE>
<P>
<HR>
<A name=gconstants></A>
<H2>Global Constants </H2>
<UL>
  <LI>Global constants should be all caps with '_' separators. </LI></UL>
<H3>Justification </H3>It's tradition for global constants to named this way. 
You must be careful to not conflict with other global <I>#define</I>s and enum 
labels. 
<H3>Example </H3><PRE>    const int A_GLOBAL_CONSTANT= 5;
</PRE>
<P>
<HR>
<A name=snames></A>
<H2>Static Variables </H2>
<UL>
  <LI>Static variables may be prepended with 's'. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>It's important to know the scope of a variable. </LI></UL>
<H3>Example </H3><PRE>   class Test
   {
   public:
   private:
      static StatusInfo msStatus;
   }
</PRE>
<P>
<HR>
<A name=tnames></A>
<H2>Type Names </H2>
<UL>
  <LI>When possible for types based on native types make a typedef. 
  <LI>Typedef names should use the same naming policy as for a class with the 
  word <I>Type</I> appended. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>Of all the different naming strategies many people found this one the best 
  compromise. 
  <LI>Types are things so should use upper case letters. <I>Type</I> is appended 
  to make it clear this is not a class. </LI></UL>
<H3>Example </H3><PRE>   typedef uint16  ModuleType;
   typedef uint32  SystemType;
</PRE>
<P>

<HR>
<A name=enames></A>
<H2>Enum Names </H2>
<H3>Labels All Upper Case with '_' Word Separators </H3>This is the standard 
rule for enum labels. 
<H4>Example </H4><PRE>   enum PinStateType {
      PIN_OFF,
      PIN_ON
   };
</PRE>
<H3>Enums as Constants without Class Scoping </H3>Sometimes people use enums as 
constants. When an enum is not embedded in a class make sure you use some sort 
of differentiating name before the label so as to prevent name clashes. 
<H4>Example </H4><PRE>   enum PinStateType  {          If <I>PIN</I> was not prepended a conflict 
                               would occur as OFF and ON are probably
      PIN_OFF,                  already defined.
      PIN_ON
   };
</PRE>
<H3>Enums with Class Scoping </H3>Just name the enum items what you wish and 
always qualify with the class name: Aclass::PIN_OFF. 
<H3>Make a Label for an Error State </H3>It's often useful to be able to say an 
enum is not in any of its <I>valid</I> states. Make a label for an uninitialized 
or error state. Make it the first label if possible. 
<H4>Example </H4><PRE>enum { STATE_ERR,  STATE_OPEN, STATE_RUNNING, STATE_DYING};
</PRE>
  <p>
<HR>
<A name=mnames></A>
<H2>#define and Macro Names </H2>
<UL>
  <LI>Put #defines and macros in all upper using '_' separators. </LI></UL>
<H3>Justification </H3>This makes it very clear that the value is not alterable 
and in the case of macros, makes it clear that you are using a construct that 
requires care. 
<P>Some subtle errors can occur when macro names and enum labels use the same 
name. 
<H3>Example </H3><PRE>#define MAX(a,b) blah
#define IS_ERR(err) blah
</PRE>
<P>
  <HR>
<A name=req></A>
<H1>Required Methods for a Class </H1>To be good citizens almost all classes 
should implement the following methods. If you don't have to define and 
implement any of the "required" methods they should still be represented in your 
class definition as comments. 
<UL>
  <LI><B>Default Constructor</B>
  <P>If your class needs a constructor, make sure to provide one. You need one 
  if during the operation of the class it creates something or does something 
  that needs to be undone when the object dies. This includes creating memory, 
  opening file descriptors, opening transactions etc. 
  <P>If the default constructor is sufficient add a comment indicating that the 
  compiler-generated version will be used. 
  <P>If your default constructor has one or more optional arguments, add a 
  comment indicating that it still functions as the default constructor. 
  <P></P>
  <LI><B>Virtual Destructor</B>
  <P>If your class is intended to be derived from by other classes then make the 
  destructor virtual. 
  <P></P>
  <LI><B>Copy Constructor</B>
  <P>If your class is copyable, either define a copy constructor and assignment 
  operator or add a comment indicating that the compiler-generated versions will 
  be used. 
  <P>If your class objects should not be copied, make the copy constructor and 
  assignment operator private and don't define bodies for them. If you don't 
  know whether the class objects should be copyable, then assume not unless and 
  until the copy operations are needed. 
  <P></P>
  <LI><B>Assignment Operator</B>
  <P>If your class is assignable, either define a assignment operator or add a 
  comment indicating that the compiler-generated versions will be used. 
  <P>If your objects should not be assigned, make the assignment operator 
  private and don't define bodies for them. If you don't know whether the class 
  objects should be assignable, then assume not. </P></LI></UL>
<P>
<H2>Justification </H2>
<UL>
  <LI>Virtual destructors ensure objects will be completely destructed 
  regardless of inheritance depth. You don't have to use a virtual destructor 
  when: 
  <UL>
    <LI>You don't expect a class to have descendants. 
    <LI>An object must have a certain data layout and size. </LI></UL>
  <LI>A default constructor allows an object to be used in an array. 
  <LI>The copy constructor and assignment operator ensure an object is always 
  properly constructed. </LI></UL>
<H2>The Law of The Big Three </H2>A class with any of (destructor, assignment 
operator, copy constructor) generally needs all 3. For more information see 
http://www.parashift.com/c++-faq-lite/coding-standards.html#[25.9]. 
<H2>Example </H2>An example using default values: <PRE>class Planet
{
public:
  // The following is the default constructor if
  // no arguments are supplied:
  //
  Planet(int radius= 5);
  
  // Use compiler-generated copy constructor, assignment, and destructor.
  // Planet(const Planet&amp;);
  // Planet&amp; operator=(const Planet&amp;);
  // ~Planet();
};
</PRE>
<P>
<HR>
  <A name=formatting></A>
  <H1>Formatting</H1>
  <HR>

<A name=brace></A>
<H2>Braces <I>{}</I> Policy </H2>
<H3>Brace Placement </H3>Of the three major brace placement strategies the
  recommended one is here: 
<UL>
  <LI>Traditional Unix policy of placing the initial brace on the same line as 
  the keyword and the trailing brace inline on its own line with the keyword: <PRE>   if (condition) {      while (condition) {
      ...                   ...
   }                     }
</PRE></LI></UL>
<H3>When Braces are Needed </H3>All if, while and do statements must either have 
braces or be on a single line. 
<P>
<H4>Always Uses Braces Form </H4>All if, while and do statements require braces 
even if there is only a single statement within the braces. For example: <PRE>if (1 == somevalue) {
   somevalue = 2;
}
</PRE>
<H4>Justification </H4>It ensures that when someone adds a line of code later 
there are already braces and they don't forget. It provides a more consistent 
look. This doesn't affect execution speed. It's easy to do. 
<H3>One Line Form </H3><PRE>if (1 == somevalue) somevalue = 2;
</PRE>
<H4>Justification </H4>It provides safety when adding new lines while maintainng 
a compact readable form. 
<H3>Add Comments to Closing Braces </H3>Adding a comment to closing braces can 
help when you are reading code because you don't have to find the begin brace to 
know what is going on. <PRE>while(1) {
   if (valid) {
  
   } // if valid
   else {
   } // not valid

} // end forever
</PRE>

<HR>
<A name=parens></A>
<H2>Parens <I>()</I> with Key Words and Functions Policy </H2>
<UL>
  <LI>Do not put parens next to keywords. Put a space between. 
  <LI>Do put parens next to function names. 
  <LI>Do not use parens in return statements when it's not necessary. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>Keywords are not functions. By putting parens next to keywords keywords 
  and function names are made to look alike. </LI></UL>
<H3>Example </H3><PRE>    if (condition) {
    }

    while (condition) {
    }

    strcpy(s, s1);

    return 1;</PRE>
<HR>
<A name=linelen></A>
<H2>A Line Should Not Exceed 78 Characters </H2>
<UL>
  <LI>Lines should not exceed 78 characters. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>Even though with big monitors we stretch windows wide our printers can 
  only print so wide. And we still need to print code. 
  <LI>The wider the window the fewer windows we can have on a screen. More 
  windows is better than wider windows. 
  <LI>We even view and print diff output correctly on all terminals and 
  printers. </LI></UL>
<P>
<HR>
  <A name=ifthen></A>
<H2><I>If Then Else</I> Formatting </H2>
<H3>Layout </H3>It's up to the programmer. Different bracing styles will yield 
slightly different looks. One common approach is: <PRE>   if (condition) {
   } else if (condition) {
   } else {
   }
</PRE>If you have <I>else if</I> statements then it is usually a good idea to 
always have an else block for finding unhandled cases. Maybe put a log message 
in the else even if there is no corrective action taken. 
<P>
<H3>Condition Format </H3>Always put the constant on the left hand side of an 
equality/inequality comparison. For example: 
<P>if ( 6 == errorNum ) ... 
<P>One reason is that if you leave out one of the = signs, the compiler will 
find the error for you. A second reason is that it puts the value you are 
looking for right up front where you can find it instead of buried at the end of 
your expression. It takes a little time to get used to this format, but then it 
really gets useful. 
<P>
<P>
<HR>
<A name=switch></A>
<H2><I>switch</I> Formatting </H2>
<UL>
  <LI>Falling through a case statement into the next case statement shall be 
  permitted as long as a comment is included. 
  <LI>The <I>default</I> case should always be present and trigger an error if 
  it should not be reached, yet is reached. 
  <LI>If you need to create variables put all the code in a block. </LI></UL>
<H3>Example </H3><PRE>   switch (...)
   {
      case 1:
         ...
      // FALL THROUGH

      case 2:
      {        
         int v;
         ...
      }
      break;

      default:
   }
</PRE>
<P>
<HR>
<A name=goto></A>
<H2>Use of <I>goto,continue,break</I> and <I>?:</I> </H2>
<H3>Goto </H3>Goto statements should be used sparingly, as in any 
well-structured code. The goto debates are boring so we won't go into them here. 
The main place where they can be usefully employed is to break out of several 
levels of switch, for, and while nesting, although the need to do such a thing 
may indicate that the inner constructs should be broken out into a separate 
function, with a success/failure return code. 
<P><PRE><TT>
   for (...) {
      while (...) {
         ...
         if (disaster) {
            goto error;</TT></PRE>
<PRE>         } <TT>
      }
   }
   ...
error:
   clean up the mess 
</TT></PRE>
<P>When a goto is necessary the accompanying label should be alone on a line and 
to the left of the code that follows. The goto should be commented (possibly in 
the block header) as to its utility and purpose. <A name=contbreak></A>
<H3>Continue and Break </H3>Continue and break are really disguised gotos so 
they are covered here. 
<P>Continue and break like goto should be used sparingly as they are magic in 
code. With a simple spell the reader is beamed to god knows where for some 
usually undocumented reason. 
<P>The two main problems with continue are: 
<UL>
  <LI>It may bypass the test condition 
  <LI>It may bypass the increment/decrement expression </LI></UL>
<P>Consider the following example where both problems occur: <PRE>while (TRUE) {
   ...
   // A lot of code
   ...
   if (/* some condition */) {
      continue;
   }
   ...
   // A lot of code 
   ...
   if ( i++ &gt; STOP_VALUE) break;
}
</PRE>Note: "A lot of code" is necessary in order that the problem cannot be 
caught easily by the programmer. 
<P>From the above example, a further rule may be given: Mixing continue with 
break in the same loop is a sure way to disaster. 
<P>
<H2>?: </H2>The trouble is people usually try and stuff too much code in between 
the <I>?</I> and <I>:</I>. Here are a couple of clarity rules to follow: 
<UL>
  <LI>Put the condition in parens so as to set it off from other code 
  <LI>If possible, the actions for the test should be simple functions. 
  <LI>Put the action for the then and else statement on a separate line unless 
  it can be clearly put on one line. </LI></UL>
<H3>Example </H3><PRE>   (condition) ? funct1() : func2();

   or

   (condition)
      ? long statement
      : another long statement;
</PRE>
<P>
  <HR>
<A name=one></A>
<H2>One Statement Per Line </H2>There should be only one statement per line 
unless the statements are very closely related. 
<P>The reasons are: 
<OL>
  <LI>The code is easier to read. Use some white space too. Nothing better than 
  to read code that is one line after another with no white space or comments. 
  </LI></OL>
<H3>One Variable Per Line </H3>Related to this is always define one variable per 
line: <PRE><B>Not:</B>
char **a, *x;

<B>Do</B>:
char **a = 0;  // add doc
char  *x = 0;  // add doc
</PRE>The reasons are: 
<OL>
  <LI>Documentation can be added for the variable on the line. 
  <LI>It's clear that the variables are initialized. 
  <LI>Declarations are clear which reduces the probablity of declaring a pointer 
  when you meant to declare just a char. </LI></OL>
<HR>
  <A name=aligndecls></A>
<H2>Alignment of Declaration Blocks </H2>
<UL>
  <LI>Block of declarations should be aligned. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>Clarity. 
  <LI>Similarly blocks of initialization of variables should be tabulated. 
  <LI>The �&amp;� and �*� tokens should be adjacent to the the name, not the type.
  </LI></UL>
<H3>Example </H3><PRE>   DWORD       aDword
   DWORD      *apDword
   char       *apChar
   char        aChar

   aDword   = 0;
   apDword  = NULL;
   apChar   = NULL;
   aChar    = 0;
</PRE>
<P>
<HR>
  <A name=classes></A>
  <H1>Classes</H1>
  <HR>
<A name=cflayout></A>
<H2>Naming Class Files</H2>
<H3>Class Definition in One File </H3>Each class definition should be in its own 
file where each file is named directly after the class's name: <PRE>   ClassName.hh
</PRE>
<H3>Implementation in One File </H3>In general each class should be implemented 
in one source file: <PRE>   ClassName.cc   // or whatever the extension is: cpp, c++
</PRE>
<H3>But When it Gets Really Big... </H3>If the source file gets too large or you 
want to avoid compiling templates all the time then add additional files named 
according to the following rule: <PRE>   ClassName_section.C
</PRE><B>section</B> is some name that identifies why the code is chunked 
together. The class name and section name are separated by '_'. 
<P>
<HR>
<A name=classlayout></A>
<H2>Class Layout </H2>A common class layout is critical from a code 
comprehension point of view and for automatically generating documentation. C++ 
programmers, through a new set of tools, can enjoy the same level generated 
documentation Java programmers take for granted. 
<P>
<H3>Class and Method Documentation </H3>It is recommended a program like
<a href="http://www.doxygen.org/">Doxygen </a>be used to document 
C++ classes, method, variables, functions, and macros. The documentation can be 
extracted and put in places in a common area for all programmers to access. This 
saves programmers having to read through class headers. Documentation generation 
should be integrated with the build system where possible. 
<P>

<H3>Required Methods Placeholders </H3>This template has placeholders for <A 
href="CppCodingStandard.html#req">required 
methods </A>. You can delete them or implement them.
<hr>
  <A name=pubpropriorder>
<H2>Ordering is: public, protected, private </H2>Notice that the public 
interface is placed first in the class, protected next, and private last. The 
reasons are: 
<UL>
  <LI>programmers should care about a class's interface more than implementation 

  <LI>when programmers need to use a class they need the interface not the 
  implementation </LI></UL>It makes sense then to have the interface first. 
Placing implementation, the private section, first is a historical accident as 
the first examples used the private first layout. Over time emphasis has 
switched deemphasizing a class's interface over implementation details. 
<H3>LIFECYCLE </H3>The life cycle section is for methods that control the life 
cycle of an object. Typically these methods include constructors, destructors, 
and state machine methods. 
<H3>OPERATORS </H3>Place all operators in this section. 
<H3>OPERATIONS </H3>Place the bulk of a class's non access and inquiry method 
methods here. A programmer will look here for the meat of a class's interface. 
<H3>ACCESS </H3>Place attribute accessors here. 
<H3>INQUIRY </H3>These are the <I>Is*</I> methods. Whenever you have a question 
to ask about an object it can be asked via in <I>Is</I> method. For example: 
IsOpen() will indicate if the object is open. A good strategy is instead of 
making a lot of access methods you can turn them around to be questions about 
the object thus reducing the exposure of internal structure. Without the 
IsOpen() method we might have had to do: if (STATE_OPEN == State()) which is 
much uglier. <A name=pubpropri>
  <hr>
  
<H2>What should go in public/protected/private? </H2>
<H3>Public Section </H3>Only put an object's interface in the public section. 
<B>DO NOT</B> expose any private data items in the public section. At least 
encapsulate access via access methods. Ideally your method interface should make 
most access methods unnecessary. Do not put data in the public interface. 
<H3>Protected and Private Section </H3>What should go into the protected section 
versus the private section is always a matter of debate. 
<H4>All Protected </H4>Some say there should be no private section and 
everything not in the public section should go in the protected section. After 
all, we should allow all our children to change anything they wish. 
<P>
<H4>All Private </H4>Another camp says by making the public interface virtual 
any derived class can change behavior without mucking with internals. 
<P>
<H4>Wishy Washy </H4>Rationally decide where elements should go and put them 
there. Not very helpful. 
<H4>And the Winner Is... </H4>Keeping everything all private seems the easiest 
approach. By making the public methods virtual flexibility is preserved.
<hr>

<H2>Method Layout </H2> <A name=mlayout></A>
The approach used is to place a comment block before each 
method that can be extracted by a tool and be made part of the class 
documentation. Here we'll use <A 
href="http://www.doxygen.org">Doxygen </A>.
See the Doxygen documentation for a list of attributes supported 
by the document generator. 
<P>
<H3>Method Header </H3>Follow Doxygen's way.
</PRE>
<hr>
<A name=namespace></A>
<H2>Use of Namespaces </H2>Namespaces are now commonly implemented by compilers. 
They should be used if you are sure your compiler supports them completely.
<P>
<H3>Naming Policy </H3>There are two basic strategies for naming: root that name 
at some naming authority, like the company name and division name; try and make 
names globally independent. 
<H3>Don't Globally Define using </H3>Don't place "using namespace" directive at 
global scope in a header file. This can cause lots of magic invisible conflicts 
that are hard to track. Keep using statements to implementation files. 
<P>
<hr>
<A name=guards></A>
<H2>Use Header File Guards </H2>Include files should protect against multiple 
inclusion through the use of macros that "guard" the files. 
<H3>When Not Using Namespces </H3><PRE>#ifndef filename_h
#define filename_h

#endif 

</PRE>The new line after the endif if is required by some compilers. 
<P>
<H3>When Using Namespaces </H4>If namespaces are used then to be completely 
safe: <PRE>#ifndef namespace_filename_h
#define namespace_filename_h

#endif 
</PRE>
<OL>
  <LI>Replace <I>filename</I> with the name of the file being guarded. This 
  should usually be the name of class contained in the file. Use the exact class 
  name. Some standards say use all upper case. This is a mistake because someone 
  could actually name a class the same as yours but using all upper letters. If 
  the files end up be included together one file will prevent the other from 
  being included and you will be one very confused puppy. It has happened! 
  <P></P>
  <LI>Most standards put a leading <B>_</B> and trailing <B>_</B>. This is no 
  longer valid as the C++ standard reserves leading _ to compiler writers. 
  <P></P>
  <LI>When the include file is not for a class then the file name should be used 
  as the guard name. 
  <P></P>
  <LI>Compilers differ on how comments are handled on preprocessor directives. 
  Historically many compilers have not accepted comments on preprocessor 
  directives. 
  <P></P>
  <LI>Historically many compilers require a new line after last endif. 
  <P></P></LI></OL>
<P>
<HR>
  
  <A name=accessor></A>
<H2>Different Accessor Styles </H2>
<H3>Why Accessors? </H3>Access methods provide access to the physical or logical 
attributes of an object. Accessing an object's attributes directly as we do for 
C structures is greatly discouraged in C++. We disallow direct access to 
attributes to break dependencies, the reason we do most things. Directly 
accessing an attribute exposes implementation details about the object. 
<P>To see why ask yourself: 
<UL>
  <LI>What if the object decided to provide the attribute in a way other than 
  physical containment? 
  <LI>What if it had to do a database lookup for the attribute? 
  <LI>What if a different object now contained the attribute? </LI></UL>If any of 
the above changed code would break. An object makes a contract with the user to 
provide access to a particular attribute; it should not promise how it gets 
those attributes. Accessing a physical attribute makes such a promise. 
<H3>Accessors Considered Somewhat Harmful </H3>At least in the public interface 
having accessors many times is an admission of failure, a failure to make an 
object's interface complete. At the protected or private level accessors are 
fine as these are the implementation levels of a class. 
<H3>Implementing Accessors </H3>There are three major idioms for creating 
accessors. 
<H4>Get/Set </H4><PRE>   class X
   {
   public:
      int    GetAge() const     { return aAge; }
      void   SetAge(int age)    { aAge= age; }
   private:
      int aAge;
   }
</PRE>The problem with Get/Set is twofold: 
<UL>
  <LI>It's ugly. Get and Set are strewn throughout the code cluttering it up. 
  <LI>It doesn't treat attributes as objects in their own right. An object will 
  have an assignment operator. Why shouldn't age be an object and have its own 
  assignment operator? </LI></UL>One benefit, that it shares with the <I>One 
Method Name</I>, is when used with messages the set method can transparently 
transform from native machine representations to network byte order. 
<H4>One Method Name </H4><PRE>   class X
   {
   public:
      int    Age() const     { return aAge; }
      void   Age(int age)    { aAge= age; }
   private:
      int aAge;
   }
</PRE>Similar to Get/Set but cleaner. Use this approach when not using the 
<I>Attributes as Objects</I> approach. 
<H4>Attributes as Objects </H4><PRE>   class X
   {
   public:
      int              Age() const     { return aAge; }
      int&amp;             rAge()          { return aAge; } 

      const String&amp;    Name() const    { return aName; }
      String&amp;          rName()         { return aName; }
   private:
      int              aAge;
      String           aName;
   }
</PRE>The above two attribute examples shows the strength and weakness of the 
Attributes as Objects approach. 
<P>When using an int type, which is not a real object, the int is set directly 
because <I>rAge()</I> returns a <B>reference</B>. The object can do no checking 
of the value or do any representation reformatting. For many simple attributes, 
however, these are not horrible restrictions. A way around this problem is to 
use a class wrapper around base types like int. 
<P>When an object is returned as reference its <I>=</I> operator is invoked to 
complete the assignment. For example: <PRE>   X x;
   x.rName()= "test";
</PRE>This approach is also more consistent with the object philosophy: the 
object should do it. An object's <I>=</I> operator can do all the checks for the 
assignment and it's done once in one place, in the object, where it belongs. 
It's also clean from a name perspective. 
<P>When possible use this approach to attribute access. 
<P>
  <HR>
<A name=initvar></A>
<H2>Initialize all Variables </H2>
<UL>
  <LI>You shall always initialize variables. Always. Every time. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>More problems than you can believe are eventually traced back to a pointer 
  or variable left uninitialized. C++ tends to encourage this by spreading 
  initialization to each constructor. </LI></UL>
<P>
<HR>
<A name=work></A>
<H2>Think About What Work to do in Constructors </H2>Should you do work that can 
fail in constructors? If you have a compiler that does not support exceptions 
(or thread safe exceptions if it matters to you) then the answer is definitely 
no.
  <A name=useopen>
<H3>Do Work in Open </H3>Do not do any real work in an object's constructor. 
Inside a constructor initialize variables only and/or do only actions that can't 
fail. 
<P>Create an Open() method for an object which completes construction. Open() 
should be called after object instantiation. 
<H4>Example </H4><PRE>   class Device
   {
   public:
      Device()    { /* initialize and other stuff */ }
      int Open()  { return FAIL; }
   };

   Device dev;
   if (FAIL == dev.Open()) exit(1);
</PRE><A name=openreasons>
<H3>Use Open Reasons </H3>
<OL>
  <LI>It is difficult to write exception safe code in constructor. It's possible 
  to throw an exception and not destruct objects allocated in the constructor. 
  Use of <B>auto_ptr</B> can help prevent this problem. 
  <LI>Some compilers do not support thread safe exceptions on all platforms. 
  <LI>Virtual methods are not available in base classes. If the base class is 
  expecting a virtual method implemented by derived classes to be available 
  during construction then initialization must follow construction. This is 
  common in frameworks. 
  <LI>Larger scale state machines may dictate when initialization should occur. 
  An object may contain numerous other objects that may have complex 
  initialization conditions. In this case we could wait to construct objects but 
  then we always have to worry about null pointers. 
  <LI>If deletion is needed to free resources we still may want to keep the 
  state around for debugging or statistics or as a supplier of information for 
  other objects. </LI></OL>
  <A name=usecon>
<H3>Do Work in Constructor </H3>With exceptions work done in the constructor can 
signal failure so it is fine to perform real work in the constructor. This is 
the guru endorced approach as a matter of fact. 
<P>The constructor code must still be very careful not to leak resources in the 
constructor. It's possible to throw an exception and not destruct objects 
allocated in the constructor. 
<P>There is a pattern called <B>Resource Acquisition as Initialization</B> that 
says all initialization is performed in the constructor and released in the 
destructor. The idea is that this is a safer approach because it should reduce 
resource leaks. 
<P>
<HR>
<A name=destexcept></A>
<H2>Be Careful Throwing Exceptions in Destructors </H2>An object is presumably 
created to do something. Some of the changes made by an object should persist 
after an object dies (is destructed) and some changes should not. Take an object 
implementing a SQL query. If a database field is updated via the SQL object then 
that change should persist after the SQL objects dies. To do its work the SQL 
object probably created a database connection and allocated a bunch of memory. 
When the SQL object dies we want to close the database connection and deallocate 
the memory, otherwise if a lot of SQL objects are created we will run out of 
database connections and/or memory. 
<P>The logic might look like: <PRE>Sql::~Sql()
{
   delete connection;
   delete buffer;
}
</PRE>
<P>Let's say an exception is thrown while deleting the database connection. Will 
the buffer be deleted? No. Exceptions are basically non-local gotos with stack 
cleanup. The code for deleting the buffer will never be executed creating a 
gaping resource leak. 
<P>Special care must be taken to catch exceptions which may occur during object 
destruction. Special care must also be taken to fully destruct an object when it 
throws an exception. 
<P>
<HR>
<A name=reuse></A>
<H1>Documentation</H1>
<A name=documentation></A>
</H1>
<HR>
<A name=cstas></A>
<H2>Comments Should Tell a Story </H2>Consider your comments a story describing 
the system. Expect your comments to be extracted by a robot and formed into a 
man page. Class comments are one part of the story, method signature comments 
are another part of the story, method arguments another part, and method 
implementation yet another part. All these parts should weave together and 
inform someone else at another point of time just exactly what you did and why.
<hr>
<A name=cdd></A>
<H2>Document Decisions </H2>Comments should document decisions. At every point 
where you had a choice of what to do place a comment describing which choice you 
made and why. 
<hr>

<A name=cuh></A>
<H2>Use Headers </H2>Use a document extraction system like <A 
href="http://www.doxygen.org">Doxygen </A>. Other sections in 
this document describe how to use ccdoc to document a class and method. 
<P>These headers are structured in such a way as they can be parsed and 
extracted. They are not useless like normal headers. So take time to fill them 
out. If you do it right once no more documentation may be necessary. 
<P>
<hr>
<A name=mge></A>
<H2>Make Gotchas Explicit </H2>Explicitly comment variables changed out of the 
normal control flow or other code likely to break during maintenance. Embedded 
keywords are used to point out issues and potential problems. Consider a robot 
will parse your comments looking for keywords, stripping them out, and making a 
report so people can make a special effort where needed. 
For a complete list of Gotcha Keywords, please refer to <a href="http://www.doxygen.org/">Doxygen </a>. Here are some useful ones:
<P>
<H3>Gotcha Keywords </H3>
<UL>
<LI><B>@author:</B><BR> specifies the author of the module <P></P>
<LI><B>@version:</B><BR> specifies the version of the module <P></P>
<LI><B>@param:</B><BR> specifies a parameter into a function <P></P>
<LI><B>@return:</B><BR> specifies what a function returns <P></P>
<LI><B>@deprecated:</B><BR> says that a function is not to be used anymore <P></P>
<LI><B>@see:</B><BR> creates a link in the documentation to the 
file/function/variable to consult to get a better understanding on what the current block of code does. 
<LI><B>@todo:</B><BR> what remains to be done<P></P>
<LI><B>@bug:</B><BR> report a bug found in the piece of code<P></P>
</LI></UL>

<P>
<H3>Gotcha Formatting </H3>
<UL>
  <LI>Make the gotcha keyword the first symbol in the comment. 
  <LI>Comments may consist of multiple lines, but the first line should be a 
  self-containing, meaningful summary. 
  <LI>The writer's name and the date of the remark should be part of the 
  comment. This information is in the source repository, but it can take a quite 
  a while to find out when and by whom it was added. Often gotchas stick around 
  longer than they should. Embedding date information allows other programmer to 
  make this decision. Embedding who information lets us know who to ask. 
</LI></UL>
<H3>Example </H3><PRE>   // :TODO: tmh 960810: possible performance problem
   // We should really use a hash table here but for now we'll
   // use a linear search.

   // :KLUDGE: tmh 960810: possible unsafe type cast
   // We need a cast here to recover the derived type. It should
   // probably use a virtual method or template.</PRE>

<A name=cdef></A>
<H2>Commenting function declarations</H2>
Functions headers should be in the file where
they are declared. This means that most likely
the functions will have a header in the .hh file. However,
functions like main() with no explicit
prototype declaration in the .hh file, should have a header
in the .cn file.
<HR>
<P>
<A name=idoc></A>
<H2>Include Statement Documentation </H2>Include statements should be 
documented, telling the user why a particular file was included. If the file 
includes a class used by the class then it's useful to specify a class 
relationship: 
<UL>
  <LI>ISA 
  <LI>HASA 
  <LI>USES </LI></UL>
<H3>Example </H3><PRE>#ifndef XX_h
#define XX_h

// SYSTEM INCLUDES
//
#include <STDIO.H>                             
#include <STRING.H>
</PRE>
<P>
  <HR>

<A name=design></A>
<H1>Using Use Cases </H1>A <I>use case</I> is a generic description of an entire 
transaction involving several objects. A use case can also describe the 
behaviour of a set of objects, such as an organization. A use case model thus 
presents a collection of use cases and is typically used to specify the behavior 
of a whole application system together with one or more external actors that 
interact with the system. 
<P>An individual use case may have a name (although it is typically not a simple 
name). Its meaning is often written as an informal text description of the 
external actors and the sequences of events between objects that make up the 
transaction. Use cases can include other use cases as part of their behaviour. 
<H2>Requirements Capture </H2>Use cases attempt to capture the requirements for 
a system in an understandable form. The idea is by running through a set of use 
case we can verify that the system is doing what it should be doing. 
<P>Have as many use cases as needed to describe what a system needs to 
accomplish. 
<H2>The Process </H2>
<UL>
  <LI>Start by understanding the system you are trying to build. 
  <LI>Create a set of use cases describing how the system is to be used by all 
  its different audiences. 
  <LI>Create a class and object model for the system. 
  <LI>Run through all the use cases to make sure your model can handle all the 
  cases. Update your model and create new use cases as necessary. </LI></UL>
<P>
<HR>
<A name=uml></A>
<H1>Unified Modeling Language </H1>The Unified Modeling Language is too large to 
present here. Fortunately you can see it at <A 
href="http://www.rational.com/ot/uml.html">Rational's </A>web site. Since you do 
need a modeling language UML is a safe choice. It combines features from several 
methods into one unified language. Remember all languages and methods are open 
to local customization. If their language is too complex then use the parts you 
and your project feel they need and junk the rest. 
<P>
<HR>
<A name=oml></A>
<H1>OPEN Method </H1><A href="http://www.markv.com/OPEN/">OPEN </A>stands for 
<B>Object-oriented Process, Environment and Notation</B> and is a worthy if not 
superior competitor to UML. It is another group effort composed of basically all 
the people not in the UML group :-) Their web site has a good comparison of OPEN 
and UML. 
<P>My guess is UML will win out for marketing reasons. But it is good to have 
some competition going. 
<P>

<HR>
<A name=open></A>
<H1>Open/Closed Principle </H1>The Open/Closed principle states a class must be 
open and closed where: 
<UL>
  <LI>open means a class has the ability to be extended. 
  <LI>closed means a class is closed for modifications other than extension. The 
  idea is once a class has been approved for use having gone through code 
  reviews, unit tests, and other qualifying procedures, you don't want to change 
  the class very much, just extend it. </LI></UL>The Open/Closed principle is a 
pitch for stability. A system is extended by adding new code not by changing 
already working code. Programmers often don't feel comfortable changing old code 
because it works! This principle just gives you an academic sounding 
justification for your fears :-) 
<P>In practice the Open/Closed principle simply means making good use of our old 
friends abstraction and polymorphism. Abstraction to factor out common processes 
and ideas. Inheritance to create an interface that must be adhered to by derived 
classes. In C++ we are talking about using <A 
href="CppCodingStandard.html#abstract">abstract 
base classes </A>. A lot. 
<P>
<HR>
<A name=contract></A>
<H1>Design by Contract </H1>The idea of design by contract is strongly related 
to <A href="CppCodingStandard.html#liskov">LSP 
</A>. A contract is a formal statement of what to expect from another party. In 
this case the contract is between pieces of code. An object and/or method states 
that it does X and you are supposed to believe it. For example, when you ask an 
object for its volume that's what you should get. And because volume is a 
verifiable attribute of a thing you could run a series of checks to verify 
volume is correct, that is, it satisfies its contract. 
<P>The contract is enforced in languages like Eiffel by pre and post condition 
statements that are actually part of the language. In other languages a bit of 
faith is needed. 
<P>Design by contract when coupled with language based verification mechanisms 
is a very powerful idea. It makes programming more like assembling spec'd parts. 
<P>

<HR>
<H1>Complexity Management</H1>
<A name=complexity></A>
<HR>
<A name=layering></A>
<H2>Layering </H2>Layering is the primary technique for reducing complexity in a 
system. A system should be divided into layers. Layers should communicate 
between adjacent layers using well defined interfaces. When a layer uses a 
non-adjacent layer then a layering violation has occurred. 
<P>A layering violation simply means we have dependency between layers that is 
not controlled by a well defined interface. When one of the layers changes code 
could break. We don't want code to break so we want layers to work only with 
other adjacent layers. 
<P>Sometimes we need to jump layers for performance reasons. This is fine, but 
we should know we are doing it and document appropriately. 
<P>
<HR>
<A name=delegation></A>
<H2>Delegation </H2>Delegation is the idea of a method using another object's 
method to do the real work. In some sense the top layer method is <I>a front</I> 
for the other method. Delegation is a form of dependency breaking. The top layer 
method never has to change while it's implementation can change at will. 
<P>Delegation is an alternative to using inheritance for implementation 
purposes. One can use inheritance to define an interface and delegation to 
implement the interface. 
<P>Some people feel delegation is a more robust form of OO than using 
implementation inheritance. Delegation encourages the formation of abstract 
class interfaces and HASA relationships. Both of which encourage reuse and 
dependency breaking. 
<H3>Example </H3><PRE>   class TestTaker
   {
   public:
      void WriteDownAnswer()   { mPaidTestTaker.WriteDownAnswer(); } 
   private:
      PaidTestTaker  mPaidTestTaker;
   }
</PRE>In this example a test taker delegates actually answering the question to 
a paid test taker. Not ethical but a definite example of delegation! 
<P>
<HR>
<A name=abstract></A>
<H2>Minimize Dependencies with Abstract Base Classes </H2>One of the most 
important strategies in C++ is to remove dependencies among different 
subsystems. Abstract base classes (ABCs) are a solid technique for dependency 
removal. 
<P>An ABC is an abstraction of a common form such that it can be used to build 
more specific forms. An ABC is a common interface that is reusable across a 
broad range of similar classes. By specifying a common interface as long as a 
class conforming to that interface is used it doesn't really matter what is the 
type of the derived type. This breaks code dependencies. New classes, conforming 
to the interface, can be substituted in at will without breaking code. In C++ 
interfaces are specified by using base classes with virtual methods. 
<P>The above is a bit rambling because it's a hard idea to convey. So let's use 
an example: We are doing a GUI where things jump around on the screen. One 
approach is to do something like: <PRE>   class Frog
   {
   public:
      void Jump();
   }
   class Bean
   {
   public:
      void Jump();
   }
</PRE>The GUI folks could instantiate each object and call the Jump method of 
each object. The Jump method of each object contains the implementation of 
jumping behavior for that type of object. Obviously frogs and beans jump 
differently even though both can jump. 
<P>Unfortunately the owner of Bean didn't like the word Jump so they changed the 
method name to Leap. This broke the code in the GUI and one whole week was lost. 

<P>Then someone wanted to see a horse jump so a Horse class was added: <PRE>   class Horse
   {
   public:
      void Jump();
   }
</PRE>The GUI people had to change their code again to add Horse. 
<P>Then someone updated Horse so that its Jump behavior was slightly different. 
Unfortunately this caused a total recompile of the GUI code and they were 
pissed. 
<P><A name=jumpable></A>Someone got the bright idea of trying to remove all the 
above dependencies using abstract base classes. They made one base class that 
specified an interface for jumping things: <PRE>   class Jumpable
   {
   public:
      virtual void Jump() = 0;
   }
</PRE>Jumpable is a base class because other classes need to derive from it so 
they can get Jumpable's interface. It's an abstract base class because one or 
more of its methods has the <I>= 0</I> notation which means the method is a 
<I>pure virtual method</I>. Pure virtual methods <B>must</B> be implemented by 
derived classes. The compiler checks. 
<P>Not all methods in an ABC must be pure virtual, some may have an 
implementation. This is especially true when creating a base class encapsulating 
a process common to a lot of objects. For example, devices that must be opened, 
diagnostics run, booted, executed, and then closed on a certain event may create 
an ABC called Device that has a method called LifeCycle which calls all other 
methods in turn thus running through all phases of a device's life. Each device 
phase would have a pure virtual method in the base class requiring 
implementation by more specific devices. This way the process of using a device 
is made common but the specifics of a device are hidden behind a common 
interface. 
<P>Back to Jumpable. All the classes were changed to derive from Jumpable: <PRE>   class Frog : public Jumpable
   {
   public:
      virtual void Jump() { ... }
   }

   etc ...
</PRE>We see an immediate benefit: we know all classes derived from Jumpable 
<B>must</B> have a Jump method. No one can go changing the name to Leap without 
the compiler complaining. One dependency broken. 
<P>Another benefit is that we can pass Jumpable objects to the GUI, not specific 
objects like Horse or Frog: <PRE>   class Gui
   {
   public:
      void MakeJump(Jumpable*);
   }

   Gui gui;
   Frog* pFrog= new Frog;
  
   gui.MakeJump(pFrog); 
</PRE>Notice Gui doesn't even know it's making a frog jump, it just has a 
jumpable thing, that's all it cares about. When Gui calls the Jump method it 
will get the implementation for Frog's Jump method. Another dependency down. Gui 
doesn't have to know what kind of objects are jumping. 
<P>We also removed the recompile dependency. Because Gui doesn't contain any 
Frog objects it will not be recompiled when Frog changes. 
<H2>Downside </H2>Wow! Great stuff! Yes but there are a few downsides: 
<H3>Overhead for Virtual Methods </H3>Virtual methods have a space and time 
penalty. It's not huge, but should be considered in design. 
<H3>Make Everything an ABC! </H3>Sometimes people overdo it, making everything 
an ABC. The rule is make an ABC when you need one not when you might need one. 
It takes effort to design a good ABC, throwing in a virtual method doesn't an 
ABC make. Pick and choose your spots. When some process or some interface can be 
reused and people will actually make use of the reuse then make an ABC and don't 
look back.
<HR>
<P>
<A name=liskov></A>
<H2>Liskov's Substitution Principle (LSP) </H2>This principle states: <PRE>   All classes derived from a base class should be interchangeable
   when used as a base class.
</PRE>The idea is users of a class should be able to count on similar behavior 
from all classes that derive from a base class. No special code should be 
necessary to qualify an object before using it. If you think about it violating 
LSP is also violating the Open/Closed 
principle because the code would have to be modified every time a derived 
class was added. It's also related to dependency management using abstract 
base classes
<P>For example, if the <A 
href="CppCodingStandard.html#jumpable">Jump 
method </A>of a Frog object implementing the Jumpable interface actually makes a 
call and orders pizza we can say its implementation is not in the spirit of Jump 
and probably all other objects implementing Jump. Before calling a Jump method a 
programmer would now have to check for the Frog type so it wouldn't screw up the 
system. We don't want this in programs. We want to use base classes and feel 
comfortable we will get consistent behaviour. 
<P>LSP is a very restrictive idea. It constrains implementors quite a bit. In 
general people support LSP and have LSP as a goal. 
<P>
<HR>
<A name=demeter></A>
<H2>Follow the Law of Demeter </H2>The <I>Law of Demeter</I> states that you 
shouldn't access a contained object directly from the containing object, you 
should use a method of the containing object that does what you want and 
accesses any of its objects as needed. 
<H3>Justification </H3>The purpose of this law is to break dependencies so 
implementations can change without breaking code. If an object wishes to remove 
one of its contained objects it won't be able to do so because some other object 
is using it. If instead the service was through an interface the object could 
change its implementation anytime without ill effect. 
<H2>Caveat </H2>As for most laws the Law of Demeter should be ignored in certain 
cases. If you have a really high level object that contains a lot of subobjects, 
like a car contains thousands of parts, it can get absurd to created a method in 
car for every access to a subobject. 
<H3>Example </H3><PRE>   class SunWorkstation
   {
   public:
      void          UpVolume(int amount) { mSound.Up(amount); }

      SoundCard     mSound;

   private:
      GraphicsCard  mGraphics;
   }

   SunWorksation sun;

   Do   : sun.UpVolume(1);
   Don't: sun.mSound.Up(1);

</PRE>


<P>
<hr>
  
<A name=miscellaneous></A>
  <H1>Miscellaneous</H1>
  <HR>
<A name=const></A>
<H2>Be Const Correct </H2>C++ provides the <I>const</I> key word to allow 
passing as parameters objects that cannot change to indicate when a method 
doesn't modify its object. Using const in all the right places is called "const 
correctness." It's hard at first, but using const really tightens up your coding 
style. Const correctness grows on you. 
<P>For more information see Const Correctness in the C++ FAQ. 
<P>
<HR>
<A name=streams></A>
<H2>Use Streams </H2>Programmers transitioning from C to C++ find stream IO 
strange preferring the familiarity of good old stdio. Printf and gang seem to be 
more convenient and are well understood. 
<P>
<H3>Type Safety </H3>Stdio is not type safe, which is one of the reasons you are 
using C++, right? Stream IO is type safe. That's one good reason to use streams. 

<P>
<H3>Standard Interface </H3>When you want to dump an object to a stream there is 
a standard way of doing it: with the <I>&lt;&lt;</I> operator. This is not true 
of objects and stdio. 
<H4>Interchangeablity of Streams </H4>One of the more advanced reasons for using 
streams is that once an object can dump itself to a stream it can dump itself to 
any stream. One stream may go to the screen, but another stream may be a serial 
port or network connection. Good stuff. 
<H4>Streams Got Better </H4>Stream IO is not perfect. It is however a lot better 
than it used to be. Streams are now standardized, acceptably efficient, more 
reliable, and now there's lots of documentation on how to use streams. 
<H4>Check Thread Safety </H4>Some stream implementations are not yet thread 
safe. Make sure that yours is. 
<H4>But Not Perfect </H4>For an embedded target tight on memory streams do not 
make sense. Streams inline a lot of code so you might find the image larger than 
you wish. Experiment a little. Streams might work on your target. 
<P>
<HR>
<A name=ifdef></A>
<H2>Use #if Not #ifdef </H2>Use #if MACRO not #ifdef MACRO. Someone might write 
code like: <PRE>#ifdef DEBUG
        temporary_debugger_break();
#endif
</PRE>Someone else might compile the code with turned-of debug info like: <PRE>cc -c lurker.cc -DDEBUG=0
</PRE>Alway use #if, if you have to use the preprocessor. This works fine, and 
does the right thing, even if DEBUG is not defined at all (!) <PRE>#if DEBUG
        temporary_debugger_break();
#endif
</PRE>If you really need to test whether a symbol is defined or not, test it 
with the defined() construct, which allows you to add more things later to the 
conditional without editing text that's already in the program: <PRE>#if !defined(USER_NAME)
 #define USER_NAME "john smith"
#endif
</PRE>
<P>
<HR>
<A name=if0></A>
<H2>Commenting Out Large Code Blocks </H2>Sometimes large blocks of code need to 
be commented out for testing. 
<H3>Using #if 0 </H3>The easiest way to do this is with an #if 0 block: <PRE>   void 
   example()
   {
      great looking code

      #if 0
      lots of code
      #endif
    
      more code
    }
</PRE>
<P>You can't use <B>/**/</B> style comments because comments can't contain 
comments and surely a large block of your code will contain a comment, won't it? 

<P>Don't use #ifdef as someone can unknowingly trigger ifdefs from the compiler 
command line. 
<H3>Use Descriptive Macro Names Instead of 0 </H3>The problem with <B>#if 
0</B>is that even day later you or anyone else has know idea why this code is 
commented out. Is it because a feature has been dropped? Is it because it was 
buggy? It didn't compile? Can it be added back? It's a mystery. 
<H3>Use Descriptive Macro Names Instead of #if 0 </H3><PRE>#if NOT_YET_IMPLEMENTED  

#if OBSOLETE

#if TEMP_DISABLED 
</PRE>
<H3>Add a Comment to Document Why </H3>Add a short comment explaining why it is 
not implemented, obsolete or temporarily disabled. 
<P>
<hr>
<A name=nooper></A>
<H2>Don't Over Use Operators </H2>C++ allows the overloading of all kinds of 
weird operators. Unless you are building a class directly related to math there 
are very few operators you should override. Only override an operator when the 
semantics will be clear to users. 
<H3>Justification </H3>
<UL>
  <LI>Very few people will have the same intuition as you about what a 
  particular operator will do. </LI></UL>
<P>
  <hr>
<A name=shortmethods></A>
<H2>Short Methods </21>
<UL>
  <LI>Methods should limit themselves to a single page of code. </LI></UL>
<H3>Justification </H3>
<UL>
  <LI>The idea is that the each method represents a technique for achieving a 
  single objective. 
  <LI>Most arguments of inefficiency turn out to be false in the long run. 
  <LI>True function calls are slower than not, but there needs to a thought out 
  decision (see premature optimization). </LI></UL>
<P>
  <hr>
  <A name=nomagic></A>
<H2>No Magic Numbers </H2>A magic number is a bare naked number used in source 
code. It's magic because no-one has a clue what it means including the author 
inside 3 months. For example: 
<P><PRE>if      (22 == foo) { start_thermo_nuclear_war(); }
else if (19 == foo) { refund_lotso_money(); }
else if (16 == foo) { infinite_loop(); }
else                { cry_cause_im_lost(); }
</PRE>In the above example what do 22 and 19 mean? If there was a number change 
or the numbers were just plain wrong how would you know? <P? <P thing. a such do 
never would they or code maintain to had has nor environment team in worked 
programmer Such else. anything than more amateur an as marks numbers magic of 
use Heavy>Instead of magic numbers use a real name that means something. You can 
use <I>#define</I> or constants or enums as names. Which one is a design choice. 
For example: <PRE>#define   PRESIDENT_WENT_CRAZY  (22)
const int WE_GOOFED= 19;
enum {
   THEY_DIDNT_PAY= 16
};

if      (PRESIDENT_WENT_CRAZY == foo) { start_thermo_nuclear_war(); }
else if (WE_GOOFED            == foo) { refund_lotso_money(); }
else if (THEY_DIDNT_PAY       == foo) { infinite_loop(); }
else                                  { happy_days_i_know_why_im_here(); }
</PRE>Now isn't that better? The const and enum options are preferable because 
when debugging the debugger has enough information to display both the value and 
the label. The #define option just shows up as a number in the debugger which is 
very inconvenient. The const option has the downside of allocating memory. Only 
you know if this matters for your application. 
<P>
<HR>
<A name=errorret></A>
<H2>Error Return Check Policy </H2>
<UL>
  <LI>Check every system call for an error return, unless you know you wish to 
  ignore errors. For example, <I>printf</I> returns an error code but rarely 
  would you check for its return code. In which case you can cast the return to 
  <B>(void)</B> if you really care. 
  <LI>Include the system error text for every system error message. 
  <LI>Check every call to malloc or realloc unless you know your versions of 
  these calls do the right thing. You might want to have your own wrapper for 
  these calls, including new, so you can do the right thing always and 
  developers don't have to make memory checks everywhere. </LI></UL>
<HR>
  <P>
<A name=useenums></A>
<H2>To Use Enums or Not to Use Enums </H2>C++ allows constant variables, which 
should deprecate the use of enums as constants. Unfortunately, in most compilers 
constants take space. Some compilers will remove constants, but not all. 
Constants taking space precludes them from being used in tight memory 
environments like embedded systems. Workstation users should use constants and 
ignore the rest of this discussion. 
<P>In general enums are preferred to <I>#define</I> as enums are understood by 
the debugger. 
<P>Be aware enums are not of a guaranteed size. So if you have a type that can 
take a known range of values and it is transported in a message you can't use an 
enum as the type. Use the correct integer size and use constants or 
<I>#define</I>. Casting between integers and enums is very error prone as you 
could cast a value not in the enum. 
<H3>A C++ Workaround </H3>C++ allows static class variables. These variables are 
available anywhere and only the expected amount of space is taken. 
<H4>Example </H4><PRE>class Variables
{
public:
   static const int   A_VARIABLE;
   static const int   B_VARIABLE;
   static const int   C_VARIABLE;
}
</PRE>
<P>
<HR>

<A name=macros></A>
<H2>Macros </H2>
<H3>Don't Turn C++ into Pascal </H3>Don't change syntax via macro substitution. 
It makes the program unintelligible to all but the perpetrator. 
<H3>Replace Macros with Inline Functions </H3>In C++ macros are not needed for 
code efficiency. Use inlines. 
<H4>Example </H4><PRE>#define  MAX(x,y)	(((x) &gt; (y) ? (x) : (y))	// Get the maximum
</PRE>
<P>The macro above can be replaced for integers with the following inline 
function with no loss of efficiency: <PRE>   inline int 
   max(int x, int y)
   {
      return (x &gt; y ? x : y);
   }
</PRE>
<H3>Be Careful of Side Effects </H3>Macros should be used with caution because 
of the potential for error when invoked with an expression that has side 
effects. 
<H4>Example </H4><PRE>   MAX(f(x),z++);
</PRE>
<H3>Always Wrap the Expression in Parenthesis </H3>When putting expressions in 
macros always wrap the expression in parenthesis to avoid potential
communitive operation abiguity. 
<H4>Example </H4><PRE>#define ADD(x,y) x + y

must be written as 

#define ADD(x,y) ((x) + (y))
</PRE>
<H3>Make Macro Names Unique </H3>Like global variables macros can
conflict with macros from other packages. 
<OL>
  <LI>Prepend macro names with package names. 
  <LI>Avoid simple and common names like MAX and MIN. </LI></OL>
<P>
<hr>
  <A name=boolean></A>
<H2>The Bull of Boolean Types </H2>Any project using source code from many 
sources knows the pain of multiple conflicting boolean types. The new C++ 
standard defines a native boolean type. Until all compilers support bool, and 
existing code is changed to use it, we must still deal with the cruel world. 
<P>The form of boolean most accurately matching the new standard is: <PRE><TT>
   typedef int     bool;
   #define TRUE    1
   #define FALSE   0

or

   const int TRUE  = 1;
   const int FALSE = 0;
</TT></PRE>Note, the standard defines the names <B>true</B> and <B>false</B> not 
TRUE and FALSE. The all caps versions are used to not clash if the standard 
versions are available. 
<P>Even with these declarations, do not check a boolean value for equality with 
1 (TRUE, YES, etc.); instead test for inequality with 0 (FALSE, NO, etc.). Most 
functions are guaranteed to return 0 if false, but only non-zero if true. Thus, <PRE><TT>
   if (TRUE == func()) { ... 
</TT></PRE>must be written <PRE><TT>
   if (FALSE != func()) { ... 
</TT></PRE>
<P>
<HR>
<A name=eassign></A>
<H2>Usually Avoid Embedded Assignments </H2>There is a time and a place for 
embedded assignment statements. In some constructs there is no better way to 
accomplish the results without making the code bulkier and less readable. 
<P><PRE><TT>
   while (EOF != (c = getchar())) 
   {
      process the character
   }
</TT></PRE>
<P>The ++ and -- operators count as assignment statements. So, for many 
purposes, do functions with side effects. Using embedded assignment statements 
to improve run-time performance is also possible. However, one should consider 
the tradeoff between increased speed and decreased maintainability that results 
when embedded assignments are used in artificial places. For example, <PRE><TT>
   a = b + c;
   d = a + r; 
</TT></PRE>should not be replaced by <PRE><TT>
   d = (a = b + c) + r; 
</TT></PRE>even though the latter may save one cycle. In the long run the time 
difference between the two will decrease as the optimizer gains maturity, while 
the difference in ease of maintenance will increase as the human memory of 
what's going on in the latter piece of code begins to fade.
<HR>
<A name=callc></A>
<H2>Mixing C and C++ </H2>In order to be backward compatible with dumb linkers 
C++'s link time type safety is implemented by encoding type information in link 
symbols, a process called <I>name mangling</I>. This creates a problem when 
linking to C code as C function names are not mangled. When calling a C function 
from C++ the function name will be mangled unless you turn it off. Name mangling 
is turned off with the <I>extern "C"</I> syntax. If you want to create a C 
function in C++ you must wrap it with the above syntax. If you want to call a C 
function in a C library from C++ you must wrap in the above syntax. Here are 
some examples:
<P>
<H3>Calling C Functions from C++ </H3><PRE>extern "C" int strncpy(...);
extern "C" int my_great_function();
extern "C"
{
   int strncpy(...);
   int my_great_function();
};
</PRE>
<H3>Creating a C Function in C++ </H3><PRE>extern "C" void
a_c_function_in_cplusplus(int a)
{
}
</PRE>
<H3><I>__cplusplus</I> Preprocessor Directive </H3>If you have code that must 
compile in a C and C++ environment then you must use the <I>__cplusplus</I> 
preprocessor directive. For example: 
<P><PRE>#ifdef __cplusplus

extern "C" some_function();

#else

extern some_function();

#endif
</PRE>
<HR>
<A name=misc></A>
<H2>Miscellaneous </H2>This section contains some miscellaneous do's and don'ts. 

<P>
<UL>
  <LI>Don't use floating-point variables where discrete values are needed. Using 
  a float for a loop counter is a great way to shoot yourself in the foot. 
  Always test floating-point numbers as &lt;= or &gt;=, never use an exact 
  comparison (== or !=). 
  <P></P>
  <LI>Compilers have bugs. Common trouble spots include structure assignment and 
  bit fields. You cannot generally predict which bugs a compiler has. You could 
  write a program that avoids all constructs that are known broken on all 
  compilers. You won't be able to write anything useful, you might still 
  encounter bugs, and the compiler might get fixed in the meanwhile. Thus, you 
  should write ``around'' compiler bugs only when you are forced to use a 
  particular buggy compiler. 
  <P></P>
  <LI>Do not rely on automatic beautifiers. The main person who benefits from 
  good program style is the programmer him/herself, and especially in the early 
  design of handwritten algorithms or pseudo-code. Automatic beautifiers can 
  only be applied to complete, syntactically correct programs and hence are not 
  available when the need for attention to white space and indentation is 
  greatest. Programmers can do a better job of making clear the complete visual 
  layout of a function or file, with the normal attention to detail of a careful 
  programmer (in other words, some of the visual layout is dictated by intent 
  rather than syntax and beautifiers cannot read minds). Sloppy programmers 
  should learn to be careful programmers instead of relying on a beautifier to 
  make their code readable. Finally, since beautifiers are non-trivial programs 
  that must parse the source, a sophisticated beautifier is not worth the 
  benefits gained by such a program. Beautifiers are best for gross formatting 
  of machine-generated code. 
  <P></P>
  <LI>Accidental omission of the second ``='' of the logical compare is a 
  problem. The following is confusing and prone to error. <PRE>        if (abool= bbool) { ... }
     </PRE>Does the programmer really mean assignment here? Often yes, but 
  usually no. The solution is to just not do it. 
  Instead use explicit tests and avoid assignment with an implicit test. The 
  recommended form is to do the assignment before doing the test: <PRE><TT>
       abool= bbool;
       if (abool) { ... }
    </TT></PRE>
  <P></P>
  <LI>Modern compilers will put variables in registers automatically. Use the 
  register sparingly to indicate the variables that you think are most critical. 
  In extreme cases, mark the 2-4 most critical values as register and mark the 
  rest as REGISTER. The latter can be #defined to register on those machines 
  with many registers. </LI></UL>
<P>
  <hr>
<A name=nodef></A>
<H2>No Data Definitions in Header Files </H2>Do not put data definitions in 
header files. for example: <PRE>/* 
 * aheader.h 
 */
int x = 0;
</PRE>
<P>
<OL>
  <LI>It's bad magic to have space consuming code silently inserted through the 
  innocent use of header files. 
  <LI>It's not common practice to define variables in the header file so it will 
  not occur to devellopers to look for this when there are problems. 
  <LI>Consider defining the variable once in a .cc file and use an extern 
  statement to reference it. 
  <LI>Consider using a singleton for access to the data. </LI></OL>
<P>
<HR>
  <A name=reentrant></A>
<H2>Make Functions Reentrant </H2>Functions should not keep static variables 
that prevent a function from being reentrant. Functions can declare variables 
static. Some C library functions in the past, for example, kept a static buffer 
to use a temporary work area. Problems happen when the function is called one or 
more times at the same time. This can happen when multiple tasks are used or say 
from a signal handler. Using the static buffer caused results to overlap and 
become corrupted. 
<P>The moral is make your functions reentrant by not using static variables in a 
function. Besides, every machine has lots of RAM now so we don't worry about 
buffer space any more :-) 
<P>
</body>
  
  # References 
  
  - https://users.ece.cmu.edu/~eno/coding/CppCodingStandard.html#classnames
