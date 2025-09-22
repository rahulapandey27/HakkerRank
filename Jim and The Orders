typedef struct {
    int id;
    int completion;
} Order;

int cmp(const void* a, const void* b) {
    Order* o1 = (Order*)a;
    Order* o2 = (Order*)b;
    if (o1->completion == o2->completion)
        return o1->id - o2->id;
    return o1->completion - o2->completion;
}

int* jimOrders(int orders_rows, int orders_columns, int** orders, int* result_count) {
    Order* arr = malloc(sizeof(Order) * orders_rows);
    for (int i = 0; i < orders_rows; i++) {
        arr[i].id = i + 1;
        arr[i].completion = orders[i][0] + orders[i][1];
    }

    qsort(arr, orders_rows, sizeof(Order), cmp);

    int* result = malloc(sizeof(int) * orders_rows);
    for (int i = 0; i < orders_rows; i++) {
        result[i] = arr[i].id;
    }

    free(arr);
    *result_count = orders_rows;
    return result;
}
