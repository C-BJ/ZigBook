# 第一章-Zig介紹

## 歡迎

[Zig](https://ziglang.org/)誕生於2016年2月，是一種通用程式設計語言和工具鏈，用於維護**健壯**、**最佳**和**可重用**的軟件。

**强大的**
- 即使對於惡劣情况（如記憶體不足）也是如此。

**最佳的**
- 讓程式以最佳管道表現和執行

**可重用的**
- 相同的程式碼適用於具有不同約束的許多環境。

**可維護的**
- 將意圖精確地傳達給編譯器和其他程式師。 該語言對人閱讀程式碼的開銷較低，並且能够靈活應對不斷變化的需求和環境。

作為新興語言代表之一的[Rust](https://rust-lang.org/)，卻早在2006年便出現，可見Zig實在非常的年輕，囙此Zig仍然是不穩定的，不推薦在生產中使用（最新主要版本是0.9，還未達到1.0，而1.0預計在2025年發佈）

要使用此書，我們假設您：

-有C/C++，Rust或類似語言的程式設計基礎（如果你會使用C#/Typescript並懂得底層程式設計知識也可以） 

-瞭解基礎算灋與資料結構

## 安裝

本指南將保證你在最新的有版本號的Zig版本中可用，但是強烈推薦你使用夜間構建版本。 因為，Zig的發佈往往間隔很久，現階段開發迅速，使用帶版本號的Zig版本可能會過時。

1.從以下位置下載並安裝Zig

[下載 ⚡ Zig Programming Language(ziglang.org)](https://ziglang.org/zh/download/)

2.將Zig所在路徑添加到環境變數

3.驗證安裝

```
$ zig version
0.10.0-dev.2951+b9ed07227
```
4.（可選）安裝ZLS和編輯器挿件

[工具 ⚡ Zig Programming Language(ziglang.org)](https://ziglang.org/zh/learn/tools/)

## Hello World

創建一個Zig檔案`main. zig`

```rust
const std = @import（“std”）；

pub fn main（）void {
    std.debug. print（“Hello World.”，. {}）；
    //std.log. info（“Hello World.”，. {}）；
}
```

###### （注意：請確保您的檔案使用空格進行縮進，LF行尾和UTF-8編碼！

使用命令編譯程式到目前的目錄：`zig build-exe main. zig`