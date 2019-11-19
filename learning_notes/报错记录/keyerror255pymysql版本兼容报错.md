报错原因：MySQL8.0更新了很多字符集，但是这些字符集长度超过255了，所以旧版的PyMySQL不支持长度超过255的字符<br>

查看当前版本：pip list，或者conda list<br/>
更新版本：pip install --upgrade PyMySQL。注意：需使用pip更新，conda更新会存在不兼容问题。
