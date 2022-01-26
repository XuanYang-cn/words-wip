# Week 1.24 - 1.28

---
## TODO - bug fix

---
## TODO - enhancement [AFTER GA]
1. Clear and Unify BaseKV interface behaviour (issue 11313)
    - Fix memoryKV load and basetable (pr 11423)
2. Test minIO inside configs rootPath (issue 11237)
    - minIO tests (pr 11255)
    - etcd
    - rocksDB
3. Milvus doesn't handle partition description now (issue 8668)
4. 推进 BaseKV enhancement #11313

## Tracking - Unmerged PR
- 11423 (memoryKV) [AFTER GA]

## TODO - Bug
- Debug: Flush hangs at e2e test after deleting datacoord or rootcoord pod kill chaos (issue 14300)
    The producers didn't recover properly
- no `_partition_name` in partition.py(issue 860)

## Timeline - In Progress

## Timeline - DONE
- Update PyMilvus tutorial.rst
- Release PyMilvus 2.0.0
