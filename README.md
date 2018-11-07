# Test nw.js version 0.34.1

This nwjs app crashes when it reaches the code line:

```App.addOriginAccessWhitelistEntry('http://github.com/', 'chrome-extension', location.host, false);```

without any error, this function addOriginAccessWhitelistEntry is being tested with different parameters but still it 
crashes, logs that it gave on cash:

```
#
# Fatal error in , line 0
# Check failed: receiver->IsJSFunction().
#
#
#
#FailureMessage Object: 0x7ffee846af200   nwjs Framework                      0x000000010dfb3a6c v8_inspector::V8StackTraceId::IsInvalid() const + 7742460
1   nwjs Framework                      0x0000000110c9597b v8_inspector::V8StackTraceId::IsInvalid() const + 54805259
2   nwjs Framework                      0x0000000110c86d85 v8_inspector::V8StackTraceId::IsInvalid() const + 54744853
3   nwjs Framework                      0x000000010d50db78 v8::internal::Object::ToInt32(int*) + 7608
4   nwjs Framework                      0x0000000111f01203 v8_inspector::V8StackTraceId::IsInvalid() const + 74120083
5   nwjs Framework                      0x000000010da901d1 v8_inspector::V8StackTraceId::IsInvalid() const + 2354017
6   nwjs Framework                      0x000000010d081e64 v8::internal::operator<<(std::__1::basic_ostream<char, std::__1::char_traits<char> >&, v8::internal::BasicBlockProfiler const&) + 130964
7   nwjs Framework                      0x000000010d0813ad v8::internal::operator<<(std::__1::basic_ostream<char, std::__1::char_traits<char> >&, v8::internal::BasicBlockProfiler const&) + 128221
8   nwjs Framework                      0x000000010d080b1a v8::internal::operator<<(std::__1::basic_ostream<char, std::__1::char_traits<char> >&, v8::internal::BasicBlockProfiler const&) + 126026
9   nwjs Framework                      0x000000010d8ebc8e v8_inspector::V8StackTraceId::IsInvalid() const + 632350
Received signal 4 <unknown> 000110c88f92
 [0x00010dfb3a6c]
 [0x00010dfb3961]
 [0x7fff6edb2f5a]
 [0x7fa0df629e5c]
 [0x00010d50db78]
 [0x000111f01203]
 [0x00010da901d1]
 [0x00010d081e64]
 [0x00010d0813ad]
 [0x00010d080b1a]
 [0x00010d8ebc8e]
[end of stack trace]
```

All the files in te crashpad folder are also attaced in the dump-files-completed folder