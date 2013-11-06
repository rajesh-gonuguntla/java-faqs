java-faqs
=========

java faqs

Q1 ) 
Write out put of the program, note that there are two compilation units
( Class Test, Other is one unit Class Other is second unit)


package testPackage;
class Test {
public static void main(String[] args) {
  String hello = "Hello", lo = "lo";
  System.out.print((hello == "Hello") + " ");
  System.out.print((Other.hello == hello) + " ");
  System.out.print((other.Other.hello == hello) + " ");
  System.out.print((hello == ("Hel"+"lo")) + " ");
  System.out.print((hello == ("Hel"+lo)) + " ");
  System.out.println(hello == ("Hel"+lo).intern());
}
}
class Other { static String hello = "Hello"; }

package other;
public class Other { public static String hello = "Hello"; }

Q2)

