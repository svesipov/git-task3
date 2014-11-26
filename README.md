git-task3
=========
Air-Sergey:git-task3 Sergey$ echo 'File task3.txt Line 1' > task3.txt

Air-Sergey:git-task3 Sergey$ echo 'File task3.txt Line 2' >> task3.txt

Air-Sergey:git-task3 Sergey$ echo 'File task3.txt Line 3' >> task3.txt

Air-Sergey:git-task3 Sergey$ echo 'File task3.txt Line 4' >> task3.txt

Air-Sergey:git-task3 Sergey$ git hash-object -w task3.txt

6898e04c9795465e9c1421e8207f5ef6638c1ba5

Air-Sergey:git-task3 Sergey$ git update-index --add task3.txt

Air-Sergey:git-task3 Sergey$ git write-tree

0aa64ca20cc8783fe371613bf54bd995c6038359

Air-Sergey:git-task3 Sergey$ echo 'commit svesipov 1' | git commit-tree 0aa64c

bbe6249763ea23131bff35470c4ed3bbbf1db5c9

Air-Sergey:git-task3 Sergey$ echo 'File task3_new.txt Line 1' > task3_new.txt

Air-Sergey:git-task3 Sergey$ echo 'File task3_new.txt Line 2' >> task3_new.txt

Air-Sergey:git-task3 Sergey$ echo 'File task3.txt (Updated) Line 1' > task3.txt

Air-Sergey:git-task3 Sergey$ echo 'File task3.txt (Updated) Line 2' >> task3.txt 

Air-Sergey:git-task3 Sergey$ echo 'File task3.txt (Updated) Line 3' >> task3.txt 

Air-Sergey:git-task3 Sergey$ echo 'File task3.txt (Updated) Line 4' >> task3.txt 

Air-Sergey:git-task3 Sergey$ git hash-object -w task3_new.txt

d22c59aa73419784fbdd29216420388428a089be

Air-Sergey:git-task3 Sergey$ git hash-object -w task3.txt

1b8eab4bf0cb329b9b72f8b814ba8e664cee72ec

Air-Sergey:git-task3 Sergey$ git update-index --add task3_new.txt

Air-Sergey:git-task3 Sergey$ git update-index --add task3.txt

Air-Sergey:git-task3 Sergey$ git write-tree

7ec413de2a0b2c527f7dc815e1a422dd1b0378e4

Air-Sergey:git-task3 Sergey$ echo 'commit svesipov 2' | git commit-tree 7ec413 -p bbe624

39555403a68327a04f182960f6a1a13d776b5335

Air-Sergey:git-task3 Sergey$ git read-tree --prefix=gittask 0aa64c

Air-Sergey:git-task3 Sergey$ git write-tree

be2a47aea5b7fa7b389dc063d64b64ea9ee512f0

Air-Sergey:git-task3 Sergey$ echo 'commit svesipov 3' | git commit-tree be2a47 -p 395554

b5862e4093858a2de883758d0a5d305da7dafafc

