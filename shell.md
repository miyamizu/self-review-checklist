## shell でログの一覧を取得するスクリプト作った

- git grep 便利
- ``で囲むと、コマンドラインを ruby で実行できる

```
# src/components で実行する

`git grep -A 5 -h "commonClickLogEvent({" | tr "\n" " " | tr -s " "`.gsub('commonClickLogEvent', "\n").each_line{ |matched|
line = matched.scan(/\({.+?}\)/)[0]
next if line.nil?
string_data = line.delete("(").delete(")")
puts string_data
result = eval(string_data)
puts "common_click_event,#{result[:name]},#{result[:component]}"
}
```
