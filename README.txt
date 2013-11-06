java-faqs
=========

java faqs
Refer Java Language Specification 7 for explanations to the answers.

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



Question 2) Write output & justify briefly.


class Test {
public static void main(String[] args) {
	int i = 1000000;
	System.out.println(i * i);
	long l = i;
	System.out.println(l * l);
	System.out.println(20296 / (l - i));
	}
}

Answer )

727379968
1000000000000
and then encounters an ArithmeticException in the division by l - i, because l
- i is zero. The first multiplication is performed in 32-bit precision, whereas the second
multiplication is a long multiplication. The value -727379968 is the decimal value of the
low 32 bits of the mathematical result, 1000000000000, which is a value too large for
type int.


Question 3) Write output, justify briefly

package TypeVarMembers;
class C {
	public void mC1()
	protected void mC2()
	void mCDefault()
	private void mC3()
}

interface I {
	void mI();
}

class CT extends C implements I {
	public void mI() {}
}

class Test {
<T extends C & I> void test(T t) {
	t.mI();

	t.mC1();
	
	t.mC2();
	t.mCDefault();
	
	t.mC3();
	
}
}

Q4) 




