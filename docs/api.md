# KitcatDB API Documentation 

This documentation describes the functions and structs made in **KitcatDB**.

## Structs

### `node`

This represents the nodes used to store key value pairs in the linked lists of the hash table.

```c
typedef struct node {
        struct node* next;
        char* key;
        char* value;
} node;
```

### `h_table` 

This represents the hash table struct of multiple linked lists.

```c
typedef struct {
        node* buckets[MAX_TABLE_SIZE];
        size_t size;
        int num_of_elements;
} h_table;
```

### node Functions

#### node* create_node(char* key, char* value);

Creates a new node with the given key and value.

Returns a pointer to the new node.

#### bool delete_node(node** head, char* target_key);

Deletes the node with the specified key from the linked list starting at head.

Returns true if the node was found and deleted, false otherwise.

#### void insert_node(node** head, node* node_to_insert);

Inserts the given node at the beginning of the linked list.

#### char* find_node(node** head, char* key);

Searches for a node with the given key in the linked list.

Returns the value associated with the key if found, NULL otherwise.

### Hash Table Functions

#### h_table* create_table(size_t size);

Creates a new hash table with the specified number of buckets (size).

Returns a pointer to the new table.

#### unsigned long hash(char* key);

Computes a hash value for the given key.

Used internally for bucket indexing.

#### bool is_valid_character(char c);

Checks if a character is valid for keys.

Returns true if valid, false otherwise.

#### bool ht_create_entry(h_table* table, char* key, char* value);

Adds a new key-value pair to the hash table.

Returns true if insertion was successful, false otherwise.

#### bool ht_delete_entry(h_table* table, char* key);

Deletes the entry with the specified key from the hash table.

Returns true if deletion was successful, false otherwise.

#### char* ht_get_entry(h_table* table, char* key);

Retrieves the value associated with the given key.

Returns the value if found, NULL otherwise.

#### float ht_lfactor(h_table* table);

Computes the current load factor of the table: num_of_elements / size.

#### void ht_rehash(h_table** table_ref);

Rehashes the table into a larger size if the load factor exceeds a threshold.

Updates the pointer to the new table.

#### h_table* ht_open(const char* ht_filename);

Loads a hash table from a .txt file.

Returns a pointer to the loaded table, or NULL if the file cannot be read.

#### bool ht_save(h_table* table, const char* ht_filename);

Saves the current table to a .txt file.

Returns true if the save was successful, false otherwise.

#### void ht_free(h_table* table);

Frees all memory associated with the hash table and its nodes.
