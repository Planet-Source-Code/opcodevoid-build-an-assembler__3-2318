<div align="center">

## Build an Assembler


</div>

### Description

This is for programmers of any langauge.This will teach you what happends to varibles and labels when they compile.Shows you example and c++ and visual basic and assembly. Teaches Opcodes and Machine code too.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[OpcodeVoid](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/opcodevoid.md)
**Level**          |Advanced
**User Rating**    |4.5 (85 globes from 19 users)
**Compatibility**  |C, C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[Complete Applications](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/complete-applications__3-7.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/opcodevoid-build-an-assembler__3-2318/archive/master.zip)





### Source Code

```
Machine code Explain Update by vbmew@hotmail
<p> Add me to your msn messenger list if you have any question
<p>
Note: if I said any thing that is wrong then tell me I will correct as soon as I can
<p>
Note again: I will give you c++ and visual basic example only
<p>
Note: i type really fast so ignore some spelling errors.
<p>
Note a more time:Please give me credit if you use this to build an assembler thx
<p>
Step 1<P>------------/////////////What is Machine code--------------\\\\\\\\\\\\\\\\\\
<p>
<p>
Machine code is somthing that the machine can only understand.
Your machine can't understand C++ or visual basic, it can only understand
Machine code. Your code is compile than link before a machine can understand it.
Lets look at a basic c++ program and see what it translate to
<p>
<p>
void main()<p>
{<p>
}
<p>
what does that assemble to, many of you have been wondering<p>
it assembles into this
<p>
push ebp
<p>
mov ebp,esp
<p>
leave
<p>
ret
<p>
I know that is assemble. Well you see if people want to understand how the machine works
they should program and assemble. Look at the assemble code of the c++ program again
now here or the Opcodes.
55 = push ebp
<p>
89E5 = nov ebp,esp
<p>
C9 = leave
<p>
C3 = ret
<p>
Yes those or Opcodes they or numbers that tell the machine what to do.
<p>
<p>
<p>
Step 2<P>--------------\\\\\\\\\\\\\ I thought computors only Knew 0's and 1's---------\\\\\\\\\\\
<p>
True computers can only understand 0's and 1's but it might not be the way you think because computors get values that way.<p>
Example:
<p>
0000-0010 = 2
<p>
when the computor see that it is going to do command number 2 which
could be retn. You see machine does not look into some memory board that contains 0101 they look at little tiny things that can be charge with 5v which means on =1 or off =0 .<p>
a computor reads the bit and tells its it on or off. A bit can hold only 1 or 0. Be on or off.
<p>
<p>
Step 3<p>-----------------\\\\\\\\\\\\ How can a Eight bits hold a value from 0-255------------------------\\\\\\\\\\\\\\\\\\\<p>
<p>
We'll many of you know that 8 bits hold a byte right. You might wonder sometimes how can 8 bits be a byte.Thats simple don't think of 8 bit as 8 bit because Eight different bits can only hold one bit each which is eight bits.
<p>
Look at them like they or together with 8*8 different Combination
Example
<p>
cpu reads these lines
<p>
0000-0001
<P>
0000-0002
<P>
0000-0003
<P>
0000-0004
<P>
0000-0005
<P>
Computor requires 255 * 5 bits or memory to read that statement. As you can see computor has to waste(not always) memory. Example go open notepad write A then save and close. Now look at it size it takes 1 byte
255 but you only put the value of 65 in there you see computors much take as much memory as the highest value you can write.<p>
As you can see the cpu is not that complex, but simple because all it can do is get 0 or 1.
<p>
Step 4<p>-------------------\\\\\\\\\\\\\\\\\\\\ When do i get to create a assembler.---------------------////////////////
<p>
Note if any tells you building a assembler is hard they or not telling the truth they or easy very easy.
<p>
how well lets take steps you might want to know what happends to
varibles when they or compile thats simple.<p>
They or store and your EXE or COM.
<p>
Look at the example below
<p>
dim I as byte<p>
I = 5
<p>
Now imagen that it compile into
<p>
0000-0001: mov ax,[0000-0003]
<p>
0000-0002: retn
<p>
0000-0003:5
<p>
As you can see varibles or store at the bottom of your exe.
As you can see many scripting langauge put the code at the buttom of a
exe because if you touch the top or the middle its offsets changes. This trows off the Cpu when trying find a varibles. This usually causes a error.
<p>
When a register(a true place where the cpu can store data) wants a varible it must goto its offset store and the exe.<p>
<p>
<p>
Now you must learn about the stack somthing else that is stored and your exe here is a little test go open up a exe with an hex editor.
<p>
you see bunch of 0's well this is the stack
<p>
And assembly you can choose your stack sizes. This is good because the more stack you have the bigger you exe is. I know what is the stack good for well if your compiling someone code and run out of register or want to save somthing for later you put it in a place called the stack like this
<p>
push ax
<p>
push bx
<p>
Those two commands push ax and bx into the stack a safe place in the exe. Here is a little test. c++ only because it has in-line assembly.
<p>
void main()<p>
{<p>
int i = 5;
<p>
asm<p>
 {
	<p>
 	push i
    <p>
 }
<p>
i = 3;
<p>
 asm<p>
 {
	<p>
	pop i
	<p>
 }
 <p>
// i now holds five again
<p>
}
<p>
Pretty cool trick it can be simulated in Other lnagauges like visual basic. Right now i'm building a dos emulator in pure vb e-mail at vbmew@hotmail.com if you want to help.
<p>
As you can see the stack is pretty cool now you really want to build a assembler, so you must learn about what happends to lables this example is in VB
<p>
goto k
<p>
K:
<p>
msgbox K
<p>
And mahcine code K would translate into Nothing thats right nothing, but goto k would translate into
<p>
jmp 1
<p>
That means jump one spaces ahead,Becuase machine can't hold labels and memory you must do that.You might be saying give me a assembler example and c++ and VB well i'm going to that now
<p>
Visual Basic example of assembler
<p>
open "Kewl.com" for output as #1
<p>
	print #1,&hc3
<p>
close #1
<p>
That writes a exe with one command. The command is return so you could do somthing like this
<p>
if CurrentCommand = "Return" then
<p>
 print#1,&hc3
<p>
end if
<p>
I know you want more commands well try this
<p>
open "Kewl.com" for output as #1
<p>
	print #1,&hb4
	<p>
	print #1,&h00
	<p>
	print #1,&hcd
	<p>
	print #1,&h16
	<p>
close #1
<p>
That waits for a keypress here is the assembly version
<p>
mov ah,0
<p>
int 16h
<p>
retn
<p>
Simple huh?
<p>
Don't worry C++ users here is your example
<p>
	ofstream fout("kewl.com");
	<P>
	fout << 0xb4;
	<p>
	fout << 0x00;
	<p>
	fout << 0xcd;
	<p>
	fout << 0x16;
 	<p>
	fout.close();
<p>
Does the same exact thing as Visual Basic.
<p>
Here is a very complicated example and Visual Basic. Note this example is not legel
Because there is no Bit type in Visual basic, i use the bit type for simplicity sake.
<p>
Dim I as bit<p>
dim J as bit<p>
I = 5<p>
J = I<p>
Now what would that assemble to. Thats simple you must increase the exe size
2 bits to hold those varibles
<p>
0000:0000 = mov ax,[0000:0004]
<p>
0000:0001 = mov bx,[0000:0005]
<p>
0000:0002 = mov ax,bx
<p>
0000:0003 = mov ax,[0000:0005]
<p>2 Bit Increase<p>
0000:0004= 5
<p>
0000:0005= 0
<p>
Now incase you don't understand here is what happends
<p>
 First we move ax(a register) to offset 0000:0004
 Which contains 5
  then we move bx to 0000:0004 which holds 0(Visual basic make unintalize varibles 0)
   now we say ax = bx. Then write it back to the exe
<p>
Of course this way is terrible you want to use the stack for this
we can simulate this in c++ like this
<p>
byte i;<p>
byte j;<p>
asm<p>
{<p>
 mov i,5<p>
 push i<p>
 pop j<p>
}
<p>
That is how it should be done, this way we can preserve memory.
<p>
<p>
Step 5<p>------------------\\\\\\\\\\\\\\\\ Understand High Level Commannds-----------////////////<p>
Here is a question many of you been wondering, "How does the compiler translate commands
 like print or cout "<P>
thats easy look at the visual basic example below
<p>
print "A"
<p>
Note i'm using one charecter only to keep it simple
<p>
here is what it assembles to
<p>
mov ah,2
<p>
mov dl,65
<p>
int 21h
<p>
Handle mutilple chars would require advance understanding of the stack and machine code
<p>
Step 6<p>-------------------\\\\\\\\\\\\\\\\\\ Example of a assembler--------------------\\\\\<p>
Here is what you all been waiting for an example assembler I will type a very very small one just to get you started<p>
<p>
Visual basic exmaple <p>
First go make c:\1.txt and put in it "quit" and new line then "quit"<p>
now open visual basic and type
<p>
dim Command as string<p>
dim Output as string 'use long if you have problems<p>
sub Compile()<p>
open "c:\1.txt" for input as #1<p>
  do while not eof(1)<p>
   line input #1,Command<p>
	<p>
  	if lcase(command) = "quit" then 'visual basic does not have case sen commands<p>
    	output = output & &hc3  <p>
	end if<p>
	loop<p>
close #1<p>
end sub<p>
<p>
sub WriteCom() 'no header<p>
 open "c:\1.com" for output as #1<p>
 	print #1,output<p>
 close #1<p>
end sub<p>
<p>
<p>
Last Step the stack<p>------------->>>>>>>>>>>>>How to pass paremeters-------->>>>>>>>>>>>>>>>>>>>>>>>>>
<p>
As you know many high level languages allow you to do statments like this
MessageBox(NULL,"Hi","Cap",MB_OK). But did you ever wonder how they pass those paremters thats easy though the stack. Here is a assembly example of the msgbox which takes 4
paremters
<p>
mov eax,NULL
<p>
mov ebx,"Hi"
<p>
mov ecx,"Cap"
<p>
mov edx,6
<p>
push edx<p>
push ecx<p>
push ebx<p>
push eax<p>
Call MessageBox<p>
As you can see we must push it in Backwords, well not quit, you see the stack is LIFO which means
<p> LAST IN FIRST OUT<P>
so the stack is like this
---------<p>
NULL<P>
-----------<p>
"HI"<P>
-----------<p>
"Cap"<p>
---------------
6<p>
----------------<p>
If we push eax first then it would be at the bottom. Here is how MessageBox reads from the stack Note you can not assemble this, statment won't work<p>
mov eax,[sp+4]<p>
push eax
<p>
2DrawMeONWindow
<p>
pop eax
<p>
mov ebx,[sp+2]
push ebx<p>
push eax<p>
SetWindowCaption<p>
pop eax<p>
pop ebx<p>
As you can see this statments not complete but it gives you a ideal on how passing paremters
work. Lets go into farther detil.
<p>
int kewl(int cool,int kool)<p>
{<p>
	cool = 3;<p>
	kool = 4;<p>
}<p>
Here is how the compiler breaks it down<p>
1.Step one Define Paremters <p>
2.Got 2, push them into stack<p>
3.Someone is using cool = 3<p>
4.cool is at the bottom of a stack size that is 2*2<p>
5.Need register eax: mov eax,[sp+4]<p>
6.Now eax holds three, no writting to exe because the varible is not global so I can let it disapear<p>
7.kool is begin used, kewl is at the top <p>
8.eax is still free so mov eax,[sp+2]<p>
9.Done<p>
Ok so it doesn't happen exacly like that but its close<p>
<p>
As you can see I brought up a new question how come global varibles stay
and locals disapear thats easy.They or never writting to the exe or push into the stack there is no need to.
<p>
Bounus Chapture some high level translation
I have tried and tried to paste them here but it wouldn't work so e-mail me with the subject
High Level. Then i will give you the commands
<p>
But i have a few i can give you on the spot
<p>
Me++;<p>
<p>
push valueofme<p>
pop ax<p>
inc ax<p>
push ax<p>
<p>
Thats Its e-mail me for more
<p><p><p>I know this is not enough to build a assembler
So if you want to build a assembler e-mail at vbmew@hotmail.com and Join the team we or building a assembler and pure vb
<P>
also i'm building one in c++ but is a high level language call blazing rain e-mail at y2j55@hotmail.com for if you want to join
<P>
<p>
<p>
Please leave feedback or vote
<P>
<p>
```

