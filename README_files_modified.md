
# Our modifications (on top of ARIABC changes) for Deterministic execution :


/src/backend/bcdb/shm_transaction.c

1. [Conflict check with other transaction](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/shm_transaction.c#L1678)

2. [Publish write-set ](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/shm_transaction.c#L1794)

/src/backend/bcdb/worker.c

1. [Initialize worker](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/worker.c#L345)

2. [Core worker logic](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/worker.c#L687)

3. [Get write-set of transaction](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/worker.c#L371)

/src/backend/access/heap/heapam.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/access/heap/heapam.c)

/src/backend/access/heap/heapam_visibility.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/access/heap/heapam_visibility.c)

/src/backend/access/transam/xact.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/access/transam/xact.c)

/src/backend/bcdb/func.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/func.c)

/src/backend/bcdb/middleware.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/middleware.c)

/src/backend/bcdb/shm_block.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/shm_block.c)

/src/backend/bcdb/worker_controller.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/bcdb/worker_controller.c)

/src/backend/executor/execMain.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/executor/execMain.c)

/src/backend/executor/nodeModifyTable.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/executor/nodeModifyTable.c)

/src/backend/nodes/tidbitmap.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/nodes/tidbitmap.c)

/src/backend/storage/lmgr/predicate.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/storage/lmgr/predicate.c)

/src/backend/tcop/postgres.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/tcop/postgres.c)

/src/backend/utils/init/globals.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/utils/init/globals.c)

/src/backend/utils/misc/postgresql.conf.sample
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/utils/misc/postgresql.conf.sample)

/src/backend/utils/resowner/resowner.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/utils/resowner/resowner.c)

/src/backend/utils/time/snapmgr.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/utils/time/snapmgr.c)

/src/include/bcdb/globals.h
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/include/bcdb/globals.h)

/src/include/bcdb/middleware.h
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/include/bcdb/middleware.h)

/src/include/bcdb/shm_block.h
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/include/bcdb/shm_block.h)

/src/include/bcdb/shm_transaction.h
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/include/bcdb/shm_transaction.h)

/src/include/bcdb/worker.h
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/include/bcdb/worker.h)

/src/backend/access/common/printtup.c
[](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/access/common/printtup.c)

# ARIABC modifications (on top of postgres) for Deterministic execution:



# New files for merkle tree creation and updating :

/src/include/access/merkle.h
[Header file](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/include/access/merkle.h)

/src/backend/access/merkle/merkleinsert.c
[Insert](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/access/merkle/merkleinsert.c)

/src/backend/access/merkle/merkleutil.c
[Util ](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/access/merkle/merkleutil.c)

/src/backend/access/merkle/merkleverify.c
[Verify](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/backend/access/merkle/merkleverify.c)

# New files for Blake 3 hash computation :

/src/include/common/blake3.h
[Header file](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/include/common/blake3.h)

/src/common/Makefile
[Makefile ](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/common/Makefile)

/src/common/blake3.c
[Core file](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/common/blake3.c)

/src/common/blake3.h
[Header file](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/common/blake3.h)

/src/common/blake3_dispatch.c
[Dispatch](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/common/blake3_dispatch.c)

/src/common/blake3_impl.h
[Implementation](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/common/blake3_impl.h)

/src/common/blake3_portable.c
[Module](https://github.com/anant7ue/safedb/blob/6e79184416322814feee48990f150145d0615756/src/common/blake3_portable.c)
