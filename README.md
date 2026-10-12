# Math Expression Parser
> Matematiksel ifadeleri recursive descent yöntemiyle ayrıştırıp hesaplayan C programı.

## Açıklama
Matematiksel ifadelerin sözdizimini recursive descent yöntemiyle analiz eden ve ifadelerin sonucunu hesaplayan bir C programıdır. İfadelerin dilbilgisi EBNF (Extended Backus–Naur Form) ile tanımlanır.

## Dilbilgisi

```
expression = term, { ("+" | "-"), term };
```

```
term = factor, { ("*" | "/"), factor };
```

```
factor 
    = LITERAL
    | "(", expression ,")"
    ;
```

## Kullanım
```bash
$ ./program "3 + 4 * 5"
23
```

```bash
$ ./program "(3 + 4) * 5"
35
```

```bash
$ ./program "10 - 2 * 3"
4
```

```bash
$ ./program "100 / (2 * 5)"
10
```

```bash
$ ./program "12 + 6 / 2 - 3"
12
```
