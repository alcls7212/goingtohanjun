# goingtohanjun

typedef struct node {
void *dataPtr;
struct node* link;
} NODE;

NODE* createNode (void* nodePtr);
#include <malloc.h>
#include <stdio.h>

#include "node.h"

NODE* createNode (void* itemPtr)
{
NODE* nodePtr = NULL;
	
nodePtr = (NODE*) malloc (sizeof (NODE)); 	
nodePtr->dataPtr = itemPtr ;
nodePtr->link = NULL
 ;
return nodePtr;
}
#include <stdio.h>
#include <malloc.h>

#include "node.h"// Header file 

int main (void)
{
int*  newData1 = NULL;
int*  newData2 = NULL;
	
NODE* node[2] = {NULL,NULL};

newData1  = (int*)malloc (sizeof (int));
*newData1 = 7;
node[0] = createNode (newData1);
node[0]->link = node[1];

newData2  = (int*)malloc (sizeof (int));
*newData2 = 75;

node[1] = createNode(newData2);

printf("Data from first node = %d\n\n",*((int*)(node[0]->dataPtr)));

printf("Data from second node = %d\n\n",*((int*)(node[1]->dataPtr)));


	
return 0;
} 
