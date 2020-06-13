# swarm-launcher


[Self-Organizing Swarm Modules | Jenkins plugin](https://plugins.jenkins.io/swarm/) を [Gradle Build Tool](https://gradle.org/) で起動。

## env

* Java 8 以降

## Swarm Option

オプションは [build.gradle](build.gradle) ファイルの args に [Available Options](https://github.com/jenkinsci/swarm-plugin#available-options) を記述してください。  
　  
主要なオプション：


|        option |  description                      | example |
| -------------:| --------------------------------- | ------------- |
| -master       | Jenkins master の URL             | http://192.168.0.1:8080
| -name         | スレーブの名前のプレフィックス     | windows-slave
| -username     | Jenkins にログインするID          |
| -password     | -username のパスワード            | 
| -fsroot       | スレーブのワークスペースルートパス | c:\\windows
| -executors    | エグゼキュータの数                | 2 
| -labels       | スレーブのラベル                  | ["windows-slave","msbuild"].join(" ")
| -mode         | 排他モード                        | exclusive  (ラベル付きジョブのみ実行)


## run


windows:

```
.\gradlew.bat
```

linux:

```
./gradlew
```


