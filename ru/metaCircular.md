# [SICP] 4.1 Метациркулярный вычислитель

https://sarabander.github.io/sicp/html/4_002e1.xhtml#g_t4_002e1

Наш интерпретатор `metaL` будет реализован как программа на `metaL`. Может
показаться неправильным думать об интерпретации программ на Лиспе с помощью
вычислителя, который сам реализован на Лиспе. Однако вычисление -- это процесс,
поэтому процесс вычисления уместно описывать с помощью Лиспа, который, в конце
концов, и является нашим инструментом для описания процессов. [207] Вычислитель,
*написанный на том же языке, какой он интерпретирует*, называется
**метациркулярным**.
