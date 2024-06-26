---
title: Storage
description:
---

## SLOAD

Original [EVM](https://www.evm.codes/#54?fork=shanghai) instruction.

Storage load operation is modeled with a native EraVM instruction.

### LLVM IR

```txt
%value = load i256, ptr addrspace(5) %pointer, align 1
```

[The LLVM IR generator code](https://github.com/matter-labs/era-compiler-llvm-context/blob/main/src/eravm/evm/storage.rs#L13)
is common for Yul and EVMLA representations.

### EraVM Assembly

```asm
sload   r1, r2
```

## SSTORE

Original [EVM](https://www.evm.codes/#55?fork=shanghai) instruction.

Storage store operation is modeled with a native EraVM instruction.

### LLVM IR

```txt
store i256 42, ptr addrspace(5) inttoptr (i256 1 to ptr addrspace(5)), align 1
```

[The LLVM IR generator code](https://github.com/matter-labs/era-compiler-llvm-context/blob/main/src/eravm/evm/storage.rs#L34)
is common for Yul and EVMLA representations.

### EraVM Assembly

```asm
sstore  r1, r2
```
