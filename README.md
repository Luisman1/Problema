#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#define MAX 50

void codificar(char string[], short int espaciado){
	short len, i;
	char string2[MAX];

	len= strlen(string);
	scanf("%hi", &espaciado);

	for(i=0; i<len; i++){
		if (string[i]==90){
			string2[i]=65+espaciado;
			printf("%c", string2[i]);
		}
		else if (string[i]==122){
			string2[i]=97+espaciado;
			printf("%c", string2[i]);
		}
		else {
			string2[i]=string[i]+espaciado;
			printf("%c", string2[i]);
		}
	}
}

int main(void) {
	char string[MAX];
	short espaciado;

	scanf("%hi", espaciado);
	scanf("%s", string);
	codificar(string, espaciado);

	return EXIT_SUCCESS;
}
