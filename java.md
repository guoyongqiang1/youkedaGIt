[增强for循环](https://ham.youkeda.com/articles/detail/5f3757005e205f30b2c2b140)

调用字符串对象方法：
>字符串长度length
取出字符串中的一个字charAt
去掉左右多余的空格trim
查找字符串indexOf
        indexOf("字符串","开始索引值"),第二个参数是一个数字类型，用于设定从什么位置开始查找。所以我们找到第一个匹配到的索引+匹配字符串长度就是开始值了，这个时候查找到的就是第二个匹配内容了
        str.indexOf("Java", index + 4)
字符串拼接substring
字符串开始和结束内容判断startsWith/endsWith
字符串替换replaceAll
字符串分割split
大小写转化toUpperCase/toLowerCase
字符串比较equals
数字和字符串转化Integer.parseInt
使用valueOf强制把数字转化为字符串

字符串转化为日期时间：
    // 把字符串转化位 LocalDate 对象，并得到字符串匹配的日期
    LocalDate date2 = LocalDate.parse("2019-01-01");
        如果日期字符串的格式不是yyyy-MM-dd,那就要借助DateTimeFormatter
        DateTimeFormatter df = DateTimeFormatter.ofPattern("yyyy/MM/dd");
        // 把字符串转化位 LocalDate 对象，并得到字符串匹配的日期
        LocalDate date2 = LocalDate.parse("2019/01/01",df);
LocalDate类方法：
                plusDays（天数）
                isBefore
                isAfter

