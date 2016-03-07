---
.. title: Issue a command to the command line
.. type: howto
---


C++ では [system](http://www.cplusplus.com/reference/cstdlib/system/) 関数を利用してシステムコマンドを実行することができます。

例えば OS X では以下のとおりです。 

```cpp
void ofApp::keyPressed(int key){
    if (key == ' '){
        system("say 'hello world'");
    }
}
```

OS によっては検討すべきオプションも存在するかもしれません。例えば POSIX システムではコマンドの末尾に & を付けることによってバックグラウンドで実行させることができます。 

examples/input\_output に入っている [systemSpeakExample](https://github.com/openframeworks/openFrameworks/tree/master/examples/input_output/systemSpeakExample) はプラットフォームごとの詳細を含めてよい参考になります。 

