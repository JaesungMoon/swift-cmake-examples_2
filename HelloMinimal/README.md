# Minimal "Hello World" Swift Example

This is a minimal CMake project demonstrating basic executable and library compilation. Refer to the HelloWorld-CMake example for a more fleshed out project file.

```
mkdir build && cd build
cmake -G Ninja ../
ninja
./hello
```

helloがmainファイル
hikitのfuncをコールしている。
なぜかわからないけどdynamic libraryだったけどstaticにしても動く

cmake の文法を理解するのが先かも、、、

HiKitというlibraryを作っている。
add_libraryというもので

header dirはbuildフォルダーをそのまま指定している。

set_target_properties(HiKit PROPERTIES
  INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_CURRENT_BINARY_DIR})
これについてはちゃんとheaderフォルダーを作って指定するのがもっと綺麗になるのかな

ninja実行前には
build.ninjaだけがある状態
build.ninjaに結構丁寧に書かれている。


CMake can not determine linker language for target: HiKit
swiftとproject level で書いてあげたらlinker languageを決めてくれた

.aの使い方をわかれば良いのかな
.dylibでも

swiftの場合はStoreKitとかをimportして使ってみたいかな、、、
dylibとしてのみあるので後から追加しないといけないのが多くあるのかな
