# typed-ffi-unsafe
Provide FFI/Unsafe for Typed/Racket

## ISSUES:
* array-set! penultimate arg is variadic: unsupported afaik in require/typed!
  * EFFECTS: array-set! only. This is the only procedure with a second-to-last variadic arg.
* CType values raise "unable to protect opaque value" deprecation warning
  * EFFECTS: All values of type CType. 
* Procedures returning late-weak-box or late-weak-hasheq are afaik unsupported!
  * EFFECTS: make-late-weakbox and make-late-hasheq. These contracts are insufficient!
* Interface insists make-late-hasheq takes zero arguments!
  * EFFECTS: make-late-hasheq only. This contract is insufficient.
