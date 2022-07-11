# heap-anti-debugger


```
void *__usercall RtlpAllocateHeap@<rax>(
        unsigned __int64 a1@<rdx>,
        __int64 a2@<rcx>,
        unsigned __int64 a3@<r8>,
        unsigned __int64 a4@<r9>,
        unsigned int a5@<r15d>,
        __int64 **a6,
        _DWORD *a7){
        
        ...
      if ( (a1 & 0x61000000) != 0 && (a1 & 0x10000000) == 0 )
      return RtlDebugAllocateHeap(a2, a1, a3);
        ...
        
        }
```


调软件bug的时候看到的
