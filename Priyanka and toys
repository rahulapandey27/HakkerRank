int compare(const void* a, const void* b){
    return(*(int*)a - *(int*)b);
}
int toys(int w_count, int* w) {
    qsort(w,w_count, sizeof(int),compare);
    int count =0;
    int i=0;
    while(i<w_count){
        count++;
        int limit=w[i]+4;
        while(i<w_count &&w[i]<=limit){
            i++;
        }
    }
    return count;
}
