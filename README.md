#include <stdio.h>

int main(void)
{
	int a;
	int b = 1;
	int fac;
	float sum = 1.0;
	int n;

	printf("1 + ");

	for (a = 2; a <= 10; a++) {
		fac = 1;
		n = 1;

		do {
			fac *= n;
			n++;
		} while (n <= a);

		if (a != 10)
			printf("%d/%d! + ", b, a);
		else
			printf("%d/%d! \n", b, a);

		sum += (float)b/fac;
		b++;
	}

	printf(" = %.8lf \n", sum);
}
