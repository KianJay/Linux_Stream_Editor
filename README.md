# Linux_Stream_Editor
Linux_Stream_Editor</br>
SED PRACTICE & EXERCISE SOLVING SOME PROBLEMS
</hr>

<h1>Questions </h1>
Solve the problems using sed</br>
1. Replace “Jon” with “Jonathan”</br>
2. Delete first 3 lines</br>
3. Delete the lines that contain “Lane”</br>
4. Print the lines for people whose birthday is Nov or Dec</br>
5. Put three asterisks (*) at the end of the line beginning with “Fred”</br>
6. Replace Popeyes’s birthday with 11/14/46</br>
7. Delete blank lines</br>
8. Write sed script with the conditions:</br>
Insert Personal File title on the first line</br>
Delete names living in San Francisco</br>
Add THE END to the last line</br>
</hr>
<h2> Answers</h2>
1. # sed -n 's/^Jon/Jonathan</br>
<img src = "https://user-images.githubusercontent.com/54985943/113116230-389c4c80-9248-11eb-8f95-358cc5f6adac.png"/>
2. # sed '1,3d' databook</br>
<img src = "https://user-images.githubusercontent.com/54985943/113116241-39cd7980-9248-11eb-83e5-ba4544d99c83.png"/>
3. # sed '/Lane/d' databook</br>
<img src = "https://user-images.githubusercontent.com/54985943/113116268-3e922d80-9248-11eb-9da2-fb949a0a3776.png"/>
4. # sed -n '/:1[12]\/[0-9]/p' databook</br>
<img src = "https://user-images.githubusercontent.com/54985943/113116274-405bf100-9248-11eb-8d6b-a1d6809724c8.png"/>
5. # sed -n '/Fred/s/.*$/&***/p' databook</br>
<img src = "https://user-images.githubusercontent.com/54985943/113116279-418d1e00-9248-11eb-8e35-c496bb270ace.png"/>
6. # sed -r -n ‘/Popeye/ s/:1?[0-9]\/[123]?[0-9]\/[0-9][0-9]:/:11\/14\/46:/p’ databook</br>
<img src = "https://user-images.githubusercontent.com/54985943/113116286-4356e180-9248-11eb-884a-c67bbc2370cb.png"/>
7. # sed ‘/^$/d’ databook</br>
<img src = "https://user-images.githubusercontent.com/54985943/113116299-4520a500-9248-11eb-8235-8e84380a9e48.png"/>
8. # cat>sedexample</br>
1i\</br>
Personal File</br>
/San Francisco/d</br>
$a\</br>
The End</br>
# sed -f sedexample databook</br>
<img src = "https://user-images.githubusercontent.com/54985943/113116312-4782ff00-9248-11eb-8732-912775057b92.png"/>
</hr>
Contributed by Duyoung Jang </br>
You can learn further details in my blog https://medium.com/kianj/linux-stream-editor-sed-d0d45f5b5537
