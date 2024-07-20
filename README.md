### 正则集合以及校验集合

#### 安装
```shell
go get github.com/jeffcail/goregs
```

#### 使用
```go
var r *GoRegs

func init() {
    r = NewGoRegs()
}

// 整数或者小数
r.MatchIntOrFloat(str string)

// 纯数字
r.MatchNumber(str string)

// 长度为n的纯数字
r.MatchLenNNumber(str string, n int)

// 长度不小于n位的纯数字
r.MatchGeNNumber(str string, n int)

// 长度m~n位的纯数字
r.MatchMNIntervalNumber(str string, m, n int)

// 非零开头的纯数字
r.MatchStartingWithNonZero(str string)

// 有n位小数的正实数
r.MatchNNovelsOfRealNumber(str string, n int)

// m~n位小数的正实数
r.MatchMNNovelsOfRealNumber(str string, m, n int)

// 非零的正整数
r.MatchNanZeroNumber(str string)

// 非零的负整数
r.MatchNanZeroNegNumber(str string)

// 长度为n的字符，特殊字符除外
r.MatchNLeCharacter(str string, n int)

// 纯英文字符串,大小写不敏感
r.MatchEnCharacter(str string)

// 纯大写英文字符串
r.MatchUpEnCharacter(str string)

// 纯小写英文字符串
r.MatchLowerEnCharacter(str string)

// 数字和26个英文字母组成的字符串,大小写不敏感
r.MatchNumberEnCharacter(str string)

// 数字和26个英文字母组成的字符串,大小写不敏感
r.MatchNumberEnUnderscores(str string)

// 密码1 由数字、26个英文字母或者下划线组成的英文开头的字符串, 长度m~n位
r.MatchPass1(str string, m, n int)

// 密码2
// 密码长度至少为8个字符。
// 包含至少一个小写字母。
// 包含至少一个大写字母。
// 包含至少一个数字。
// 包含至少一个特殊字符（例如 !@#$%^&*() 等
r.MatchPass2(str string)

// 验证是否包含特殊字符串
r.MatchIsContainSpecialCharacter(str string)

// 纯汉字
r.MatchChineseCharacter(str string)

// email
r.MatchEmail(str string)

// 大陆手机号
r.MatchChinesePhoneNumber(str string)

// 验证大陆身份证号
r.MatchChineseIDCardNumber(id string)

// 大陆手机号
r.MatchContainChineseCharacter(str string)

// 匹配双字节字符(包括汉字在内)
r.MatchDoubleByte(input string)

// 匹配零个或多个空白字符（包括空格、制表符、换页符等）
r.MatchEmptyLine(input string)

// ipv4
r.MatchIPv4(input string)

// ipv6
r.MatchIPv6(input string)
```