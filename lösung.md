Benjamin Besic 3AHIF

# Free Blocks Management

## 1.)
| Block      | 17      | 18     |
|------------|---------|--------|
| Next Block | 18      | 0      |
|            | 4589    | 24353  |
|            | 43536   | 98745  |
|            | 718     | 76345  |
|            | 345     | 9877   |
|            | 23456   | 7345   |
|            | 8345345 | 34535  |
|            | 634534  | 154698 |
|            | 3478    | 967    |
|            | 56      | 8657   |

### a) Five new blocks are allocated
| Block      | 17      | 18     |
|------------|---------|--------|
| Next Block | 18      | 0      |
|            | 4589    | 24353  |
|            | 43536   | 98745  |
|            | 718     | 76345  |
|            | 345     | 9877   |
|            | <mark></mark>    | 7345   |
|            | <mark></mark>  | 34535  |
|            | <mark></mark> | 154698 |
|            | <mark></mark>     | 967    |
|            | <mark></mark>     | 8657   |

### b) The block 22 is freed
| Block      | 17      | 18     |
|------------|---------|--------|
| Next Block | 18      | 0      |
|            | 4589    | 24353  |
|            | 43536   | 98745  |
|            | 718     | 76345  |
|            | 345     | 9877   |
|            | <mark>22</mark>      | 7345   |
|            |  | 34535  |
|            | | 154698 |
|            |     | 967    |
|            |     | 8657   |

### c) Another 5 blocks are allocated
| Block      | 17      | 18     |
|------------|---------|--------|
| Next Block | 18      | 0      |
|            | <mark></mark>   | 24353  |
|            | <mark></mark>  | 98745  |
|            |  <mark></mark>   | 76345  |
|            |  <mark></mark>   | 9877   |
|            |  <mark></mark>    | 7345   |
|            |  | 34535  |
|            | | 154698 |
|            |     | 967    |
|            |     | 8657   |

### d) Another block is allocated
| Block      | <mark>18</mark>     |
|------------|--------|
| Next Block | 0      |
|            | 24353  |
|            | 98745  |
|            | 76345  |
|            | 9877   |
|            | 7345   |
|            | 34535  |
|            | 154698 |
|            | 967    |
|            |   17   |


### e) Another three blocks are allocated
| Block      | 18     |
|------------|--------|
| Next Block | 0      |
|            | 24353  |
|            | 98745  |
|            | 76345  |
|            | 9877   |
|            | 7345   |
|            | 34535  |
|            | <mark></mark>  |
|            |  <mark></mark>   |
|            |  <mark></mark>    |

### f) Four blocks(23456,8345345,56 and 634534) are freed
| Block      | <mark>56</mark>  | 18     |
|------------|---------|--------|
| Next Block | 18      | 0      |
|            |         | 24353  |
|            |         | 98745  |
|            |         | 76345  |
|            |         | 9877   |
|            |         | 7345   |
|            |         | 34535  |
|            |         | 23456  |
|            |         | 8345345|
|            |         | 634534 |


## 2.)
### Given the two memory footprint scenarios for Free Blocks Managment as presented in class. State the condition under which the linked list approach uses less space than the bitmap approach.

The linked list approach uses less if you have so much data allocated that the amount you
need for free blocks management decreases so much that it's lower than the constant bit vector amount required for free blocks management.
