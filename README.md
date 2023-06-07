// 20213114 이화창

/*
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

struct Book {
	int number;
	char title[100];
};

int main(void){

	struct Book*p;

	p=(struct Book*)malloc(2* sizeof(struct Book));

	if(p==NULL){
		printf("메모리할당오류\n");
		exit(1);
	}
	p[0].number = 1;  // (*p).number = 1
	        strcpy(p[0].title, "C Programming");

	        p[1].number = 2;// (*p+1).number = 2
	        strcpy(p[1].title, "Data Structure");

	        free(p);
	        return 0;
	}
}
*/
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

struct movie{
	char title[100];
	double rating;
};

int main(void){
	struct movie*ptr;
	int i,n;


	printf("영화의 개수 ");
	scanf("%d",&n);
	getchar();

	ptr=(struct movie*)malloc(n*sizeof(struct movie));
	if(ptr==NULL){
		printf("메모리 할당 오류\n")
		exit(1);
	}

	for(i=0; i<n; i++){
		printf("영화의 제목:");
		get_s(ptr[i].title, 100);

		printf("영화 평점:");
		scanf("%lf", &ptr[i].rating);
		getchar();

	printf("\n===========================\n");
	for(i=0; i<n; i++){
		printf("영화제목:%s\n", ptr[i].title);
		printf("영화 평점:%lf\n", ptr[i].rating);
	}
	printf("===========================\n");
	free(ptr);
	return 0;
	}







