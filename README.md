#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node* next;
};

int main() {
    struct node *head, *temp;

    head = (struct node*)malloc(sizeof(struct node));
    printf("Enter data for node: ");
    scanf("%d", &head->data);
    head->next = NULL;

    temp = head;
    head = head->next;
    free(temp);

    printf("First node deleted");

    return 0;
}
