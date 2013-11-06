java-faqs
=========

java faqs

Question 1)

Write output using the following two compilation units.
-- compilation unit 1
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

-- Compilation unit 2
package other;
public class Other { public static String hello = "Hello"; }

Answer )
true true true true false true

=======
>>>>>>> b603ecd4e95bf92f09978ea858353a62799ad508


