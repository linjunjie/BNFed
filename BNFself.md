#BNF定义BNF自身

syntax			::=	{ rule }
rule			::= identifier "::=" expression
expression		::= term { "|" term }
term			::= factor { factor }
factor			::= identifier | quoted_symbol | "(" expression ")" | "[" expression "]" | "{" expression "}"
identifier		::= letter { letter | digit }
quoted_symbol	::= """ { any_character } """