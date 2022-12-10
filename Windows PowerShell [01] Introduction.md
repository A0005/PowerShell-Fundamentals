<h1>Windows PowerShell [01] Introduction</h1>

[YouTube Demonstration](https://www.youtube.com/watch?v=TUNNmVeyjW0&list=PL1H1sBF1VAKXqO_N3ZNP0aL15miJcUhw7)

<h2>Description</h2>
This is an introduction lesson in learning how to use PowerShell.
<br />


<h2>Languages</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Virtual Box</b>
- <b>Windows 11</b>

<h2>Lesson walk-through:</h2>

<!-- <p align="center"> --!>
1 - In PowerShell to find out your current directory simply type "cd ."
<img width="700" alt="cd in Powershell" src="https://user-images.githubusercontent.com/103763124/206520970-c46df546-48b2-437c-9137-3e17e1f92013.png">
<br />
<br />
2	- In PowerShell you can move up a directory which is your parent directory by simply typing "cd .."
<img width="700" alt="cd   in PowerShell" src="https://user-images.githubusercontent.com/103763124/206522052-9b48244d-ac23-41ce-b3b1-c24aa16cd26c.png">
<br />
<br />
3	- In PowerShell you can type "dir" to get the directory listing of the current directory that you are in.
<img width="700" alt="dir in PowerShell" src="https://user-images.githubusercontent.com/103763124/206523007-c09f1085-aa94-4aa8-abfe-c259e95d4b95.png">
<br />
<br />
4	- But the proper Cmdlet to use in PowerShell to get the directory listing of the current directory is "Get-ChildItem"
<img width="700" alt="Get-ChildItem in PowerShell" src="https://user-images.githubusercontent.com/103763124/206524756-81eec5eb-3afc-42f5-9861-c8b3d0f93689.png">
<br />
<br />
5	- To move from the directory that you are currently in into another directory simply type "cd *following the directory’s name*" - Here will move from the users directory into the member directory. The proccees of typing "cd Member" is called a Relative Path.
<img width="700" alt="cd Member PowerShell" src="https://user-images.githubusercontent.com/103763124/206526088-e25c69c7-af18-4bcf-93ce-c1b80fb93a89.png">
<br />
<br />
6	- We can also use an Absolute Path which can be going from the very root of the file system or any dirve to a specific directory that you want. For example here will go back to the Users directory by typing "cd C:\Users"
<img width="700" alt="Absolute path in Powershell" src="https://user-images.githubusercontent.com/103763124/206527765-a476539c-1b3e-4b99-8ffd-5aa830d1c67b.png">
<br />
<br />
7	- If you are used to using Linux and Unix commands you can simply type "Get-Alias" and it will show you the Aliases that you are used to using in Linux\Unix systems with the corresponding Cmdlet used in PowerShell.
<img width="700" alt="Get-Alias in PowerShell" src="https://user-images.githubusercontent.com/103763124/206530832-d6ab6c5a-27ec-4dd1-839d-fb4640ab2423.png">
<br />
<br />
8	- What differs PowerShell from any other system shell is that in PowerShell you will be working with objects. Here we are going to get the listings of the current directory and pipe (|) it into another Cmdlet. For example by typing "Get-ChildItem | Select-Object Name" this will return what is under the object name.
<img width="700" alt="Select-Object in PowerShell" src="https://user-images.githubusercontent.com/103763124/206532161-30ce5286-4ae6-47a4-bbb0-3b9f6f646245.png">
<br />
<br />
9	- We can customize the pervious Cmdlet depending on what we want to achieve. Typing "Get-ChildItem | Select-Object -First 1" will output the first object in the director’s listing.
<img width="700" alt="SelectObject First 1 PowerShell" src="https://user-images.githubusercontent.com/103763124/206557873-007f5c07-5eb1-4b6b-b687-715fb91af7d8.png">
<br />
<br />
10	- As the pervious Cmdlet Typing "Get-ChildItem | Select-Object -Index 0" will also output the first object in the directory’s listing. But here will go further by piping in another Cmdlet. Typing "Get-ChildItem | Select-Object -First 1 | Select-Object Name" will return only the name object from the first object.
<img width="700" alt="Index 0 PowerShell" src="https://user-images.githubusercontent.com/103763124/206558801-3b375b11-2282-4986-a1ce-f67e0e3ff4a9.png">
<br />
<br />
11	- Typing "Get-ChildItem | Select-Object -Index 0 | Get-Member" will show you more information about what that object requires.
<img width="700" alt="GetMember PowerShell" src="https://user-images.githubusercontent.com/103763124/206560081-9fafe3ec-1120-477f-81ad-4ad07c1002c0.png">
<br />
<br />
12	- So the reason we use the pervious Cmdlet with "Get-Member" is because all objects in a directory will not be listed. So, for example to find out the Root or Parent of an object we can type "Get-ChildItem | Select-Object -First 1 | Select-Object Parent" - To simplify this Cmdlet we can use an alias for "Select-Object" which will be "Select" for example "Get-ChildItem | Select -First 1 | Select Parent".
<img width="700" alt="Select Parent PowerShell" src="https://user-images.githubusercontent.com/103763124/206561580-b3f48411-8fac-4eef-a4e7-71c758b2910b.png">
<br />
<br />
13	- In this example we will use the Cmdlet in a programming way that most people are used to by adding parentheses like a C# style. For example "(Get-ChildItem | Select -First 1).Name" this will output the contents without the PowerShell header.
<img width="700" alt="Name PowerShell" src="https://user-images.githubusercontent.com/103763124/206563162-ef2bfc9e-6781-457a-9053-b8de5c447538.png">
<br />
<br />
14	- Another option we can use is Methods. For example "(Get-ChildItem | Select -First 1).ToString()" this will also output the contents without the PowerShell header. There are many different options we can use to get the most out of PowerShell and we can explore these options in "Get-Member".
<img width="700" alt="ToString PowerShell" src="https://user-images.githubusercontent.com/103763124/206566141-a03e05c4-8267-4170-b517-b51023ae071b.png">
<br />
<br />
15	- To learn a little more about a Cmdlet we can Type "Get-Help" follwing the Cmdlet. This is like the man page that we use is Linux but for PowerShell. 
<img width="700" alt="GetHelp PowerShell" src="https://user-images.githubusercontent.com/103763124/206567423-296b0858-8d0f-4d2a-9099-705934285af1.png">
<br />
<br />
16	- If you do not know the Cmdlet that you are looking for, for example a printer Cmdlet you can type "Get-Help *printer*" and it will show you Cmdlets that you can run in PowerShell.
<img width="700" alt="GetHelp Printer PowerShell" src="https://user-images.githubusercontent.com/103763124/206568021-bdd24b0c-cb7a-4193-b7e6-83e326b0dbcc.png">
<br />
<br />
17	- Another example you can use wtih "Get-Help" is "Get-Help *network*" this will show you more information on differerent network Cmdlets you can use.
<img width="700" alt="GetHelp Network PowerShell" src="https://user-images.githubusercontent.com/103763124/206854605-3feefdad-c6e6-47ef-986b-1032254ce650.png">
<br />
<br />
18	- Using the following Cmdlet "Get-Command" will show you all the Cmdlets that you can use within PowerShell.
<img width="700" alt="GetCommand PowerShell" src="https://user-images.githubusercontent.com/103763124/206854754-6514cfc3-852c-45b7-917a-37b6b124aed0.png">
<br />
<br />
19	- Using the "Get-Command *printer*" will show printer Cmdlets you can use within PowerShell.
<img width="700" alt="GetCommand Printer PowerShell" src="https://user-images.githubusercontent.com/103763124/206854849-577a65c1-3c0b-49e5-9a76-69a3b7239461.png">
<br />
<br />
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
