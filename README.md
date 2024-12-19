# git-project2
#include<stdio.h>
#include<stdbool.h>

struct TASK{
    int ID;
    char word[50];
    int  priorety;
    struct TASK*next;
};
typedef struct TASK*ListTASK;

bool Search_Task(int XID,ListTASK X) {
    ListTASK Q=X;
    while (Q!=NULL){
        if (Q->ID == XID)
              return true;
        else Q=Q->next;
    }
    return false;

}