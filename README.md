
Conversation opened. 14 messages. All messages read.

Skip to content
Using Gmail with screen readers
14 of 389
visual basic code
Inbox
tshingombe fiston <tshingombefiston@gmail.com>
	
Fri, Apr 5, 10:25 AM (6 days ago)
	
to me, TSHINGOMBEKB, tshigombekb
Main menu













Wikipedia The Free Encyclopedia

    Create account
    Log in 

Personal tools



Africa Creates! 
Now Open! Enter your photos, video and audio in the annual celebration of Africa! 
Hide
Contents


    Cross-platform and open-source development
    See also
    References
    Further reading
    External links

Visual Basic (.NET)

    Article
    Talk

    Read
    Edit
    View history

Tools

















From Wikipedia, the free encyclopedia
This article is about the modern programming language for .NET. For the original Visual Basic, the last version of which was Visual Basic 6.0, see Visual Basic (classic).
Visual Basic
Paradigm	Multi-paradigm: structured, imperative, object-oriented, declarative, generic, reflective and event-driven
Designed by	Microsoft
Developer	Microsoft
First appeared	2001; 23 years ago

Stable release	
17.9.2[1] Edit this on Wikidata / 27 February 2024; 38 days ago
Typing discipline	Static, both strong and weak,[2] both safe and unsafe,[2] nominative
Platform	.NET Framework, Mono, .NET[3][4]
OS	Chiefly Windows
Also on Android, BSD, iOS, Linux, macOS, Solaris, and Unix
License	Roslyn compiler: Apache License 2.0[5]
Filename extensions	.vb
Website	docs.microsoft.com/dotnet/visual-basic/
Major implementations
.NET Framework SDK, Roslyn Compiler and Mono
Dialects
Microsoft Visual Basic
Influenced by
Classic Visual Basic
Influenced
Small Basic, Mercury

Visual Basic (VB), originally called Visual Basic .NET (VB.NET), is a multi-paradigm, object-oriented programming language, implemented on .NET, Mono, and the .NET Framework. Microsoft launched VB.NET in 2002 as the successor to its original Visual Basic language, the last version of which was Visual Basic 6.0. Although the ".NET" portion of the name was dropped in 2005, this article uses "Visual Basic [.NET]" to refer to all Visual Basic languages released since 2002, in order to distinguish between them and the classic Visual Basic. Along with C# and F#, it is one of the three main languages targeting the .NET ecosystem. Microsoft updated its VB language strategy on 6 February 2023, stating that VB is a stable language now and Microsoft will keep maintaining it.[6]

Microsoft's integrated development environment (IDE) for developing in Visual Basic is Visual Studio. Most Visual Studio editions are commercial; the only exceptions are Visual Studio Express and Visual Studio Community, which are freeware. In addition, the .NET Framework SDK includes a freeware command-line compiler called vbc.exe. Mono also includes a command-line VB.NET compiler.

Visual Basic is often used in conjunction with the Windows Forms GUI library to make desktop apps for Windows. Programming for Windows Forms with Visual Basic involves dragging and dropping controls on a form using a GUI designer and writing corresponding code for each control.
Use in making GUI programs
See also: Windows Forms

The Windows Forms library is most commonly used to create GUI interfaces in Visual Basic. All visual elements in the Windows Forms class library derive from the Control class. This provides the minimal functionality of a user interface element such as location, size, color, font, text, as well as common events like click and drag/drop. The Control class also has docking support to let a control rearrange its position under its parent.

Forms are typically designed in the Visual Studio IDE. In Visual Studio, forms are created using drag-and-drop techniques. A tool is used to place controls (e.g., text boxes, buttons, etc.) on the form (window). Controls have attributes and event handlers associated with them. Default values are provided when the control is created, but may be changed by the programmer. Many attribute values can be modified during run time based on user actions or changes in the environment, providing a dynamic application. For example, code can be inserted into the form resize event handler to reposition a control so that it remains centered on the form, expands to fill up the form, etc. By inserting code into the event handler for a keypress in a text box, the program can automatically translate the case of the text being entered, or even prevent certain characters from being inserted.
Syntax
[icon]	
This section needs expansion. You can help by adding to it. (April 2014)

Visual Basic uses statements to specify actions. The most common statement is an expression statement, consisting of an expression to be evaluated, on a single line. As part of that evaluation, functions or subroutines may be called and variables may be assigned new values. To modify the normal sequential execution of statements, Visual Basic provides several control-flow statements identified by reserved keywords. Structured programming is supported by several constructs including two conditional execution constructs (If ... Then ... Else ... End If and Select Case ... Case ... End Select ) and four iterative execution (loop) constructs (Do ... Loop, For ... To, For Each, and While ... End While) . The For ... To statement has separate initialisation and testing sections, both of which must be present. (See examples below.) The For Each statement steps through each value in a list.

In addition, in Visual Basic:

    There is no unified way of defining blocks of statements. Instead, certain keywords, such as "If … Then" or "Sub" are interpreted as starters of sub-blocks of code and have matching termination keywords such as "End If" or "End Sub".
    Statements are terminated either with a colon (":") or with the end of line. Multiple-line statements in Visual Basic are enabled with " _" at the end of each such line. The need for the underscore continuation character was largely removed in version 10 and later versions.[7]
    The equals sign ("=") is used in both assigning values to variables and in comparison.
    Round brackets (parentheses) are used with arrays, both to declare them and to get a value at a given index in one of them. Visual Basic uses round brackets to define the parameters of subroutines or functions.
    A single quotation mark (') or the keyword REM, placed at the beginning of a line or after any number of space or tab characters at the beginning of a line, or after other code on a line, indicates that the (remainder of the) line is a comment.

Simple example

The following is a very simple Visual Basic program, a version of the classic "Hello, World!" example created as a console application:

Module Module1

    Sub Main()
        ' The classic "Hello, World!" demonstration program
        Console.WriteLine("Hello, World!")
    End Sub

End Module

It prints "Hello, World!" on a command-line window. Each line serves a specific purpose, as follows:

Module Module1

This is a module definition. Modules are a division of code, which can contain any kind of object, like constants or variables, functions or methods, or classes, but can not be instantiated as objects like classes and cannot inherit from other modules. Modules serve as containers of code that can be referenced from other parts of a program.[8]
It is common practice for a module and the code file which contains it to have the same name. However, this is not required, as a single code file may contain more than one module or class.

Sub Main()

This line defines a subroutine called "Main". "Main" is the entry point, where the program begins execution.[9]

Console.WriteLine("Hello, world!")

This line performs the actual task of writing the output. Console is a system object, representing a command-line interface (also known as a "console") and granting programmatic access to the operating system's standard streams. The program calls the Console method WriteLine, which causes the string passed to it to be displayed on the console.

Instead of Console.WriteLine, one could use MsgBox, which prints the message in a dialog box instead of a command-line window.[10]
Complex example

This piece of code outputs Floyd's Triangle to the console:

Imports System.Console

Module Program

    Sub Main()
        Dim rows As Integer

        ' Input validation.
        Do Until Integer.TryParse(ReadLine("Enter a value for how many rows to be displayed: " & vbcrlf), rows) AndAlso rows >= 1
            WriteLine("Allowed range is 1 and {0}", Integer.MaxValue)
        Loop
      
        ' Output of Floyd's Triangle
        Dim current As Integer = 1
        Dim row As Integer 
        Dim column As Integer
        For row = 1 To rows
            For column = 1 To row
                Write("{0,-2} ", current)
                current += 1
            Next

            WriteLine()
        Next
    End Sub

    ''' <summary>
    ''' Like Console.ReadLine but takes a prompt string.
    ''' </summary>
    Function ReadLine(Optional prompt As String = Nothing) As String
        If prompt IsNot Nothing Then
            Write(prompt)
        End If

        Return Console.ReadLine()
    End Function

End Module

Comparison with the classic Visual Basic
Main article: Comparison of Visual Basic and Visual Basic .NET

Whether Visual Basic .NET should be considered as just another version of Visual Basic or a completely different language is a topic of debate. There are new additions to support new features, such as structured exception handling and short-circuited expressions. Also, two important data-type changes occurred with the move to VB.NET: compared to Visual Basic 6, the Integer data type has been doubled in length from 16 bits to 32 bits, and the Long data type has been doubled in length from 32 bits to 64 bits. This is true for all versions of VB.NET. A 16-bit integer in all versions of VB.NET is now known as a Short. Similarly, the Windows Forms editor is very similar in style and function to the Visual Basic form editor.

The things that have changed significantly are the semantics—from those of an object-based programming language running on a deterministic, reference-counted engine based on COM to a fully object-oriented language backed by the .NET Framework, which consists of a combination of the Common Language Runtime (a virtual machine using generational garbage collection and a just-in-time compilation engine) and a far larger class library. The increased breadth of the latter is also a problem that VB developers have to deal with when coming to the language, although this is somewhat addressed by the My feature in Visual Studio 2005.

The changes have altered many underlying assumptions about the "right" thing to do with respect to performance and maintainability. Some functions and libraries no longer exist; others are available, but not as efficient as the "native" .NET alternatives. Even if they compile, most converted Visual Basic 6 applications will require some level of refactoring to take full advantage of the new language. Documentation is available to cover changes in the syntax, debugging applications, deployment and terminology.[11]
Comparative examples

The following simple examples compare VB and VB.NET syntax. They assume that the developer has created a form, placed a button on it and has associated the subroutines demonstrated in each example with the click event handler of the mentioned button. Each example creates a "Hello, World" message box after the button on the form is clicked.

Visual Basic 6:

Private Sub Command1_Click()
    MsgBox "Hello, World"
End Sub

VB.NET (MsgBox or MessageBox class can be used):

Private Sub Button1_Click(sender As object, e As EventArgs) Handles Button1.Click
    MsgBox("Hello, World")
End Sub

    Both Visual Basic 6 and Visual Basic .NET automatically generate the Sub and End Sub statements when the corresponding button is double-clicked in design view. Visual Basic .NET will also generate the necessary Class and End Class statements. The developer need only add the statement to display the "Hello, World" message box.
    All procedure calls must be made with parentheses in VB.NET, whereas in Visual Basic 6 there were different conventions for functions (parentheses required) and subs (no parentheses allowed, unless called using the keyword Call).
    The names Command1 and Button1 are not obligatory. However, these are default names for a command button in Visual Basic 6 and VB.NET respectively.
    In VB.NET, the Handles keyword is used to make the sub Button1_Click a handler for the Click event of the object Button1. In Visual Basic 6, event handler subs must have a specific name consisting of the object's name ("Command1"), an underscore ("_"), and the event's name ("Click", hence "Command1_Click").
    There is a function called MessageBox.Show in the Microsoft.VisualBasic namespace which can be used (instead of MsgBox) similarly to the corresponding function in Visual Basic 6. There is a controversy[12] about which function to use as a best practice (not only restricted to showing message boxes but also regarding other features of the Microsoft.VisualBasic namespace). Some programmers prefer to do things "the .NET way", since the Framework classes have more features and are less language-specific. Others argue that using language-specific features makes code more readable (for example, using int (C#) or Integer (VB.NET) instead of System.Int32).
    In Visual Basic 2008, the inclusion of ByVal sender as Object, ByVal e as EventArgs has become optional.

The following example demonstrates a difference between Visual Basic 6 and VB.NET. Both examples close the active window.

Visual Basic 6:

Sub cmdClose_Click()
    Unload Me
End Sub

VB.NET:

Sub btnClose_Click(sender As Object, e As EventArgs) Handles btnClose.Click
    Close()
End Sub

The 'cmd' prefix is replaced by the 'btn' prefix, conforming to the new convention previously mentioned.[which?]

Visual Basic 6 did not provide common operator shortcuts. The following are equivalent:

Visual Basic 6:

Sub Timer1_Timer()
    'Reduces Form Height by one pixel per tick
    Me.Height = Me.Height - 1
End Sub

VB.NET:

Sub Timer1_Tick(sender As Object, e As EventArgs) Handles Timer1.Tick
    Me.Height -= 1
End Sub

Comparison with C#
Main article: Comparison of C Sharp and Visual Basic .NET

C# and Visual Basic are Microsoft's first languages made to program on the .NET Framework (later adding F# and more; others have also added languages). Though C# and Visual Basic are syntactically different, that is where the differences mostly end. Microsoft developed both of these languages to be part of the same .NET Framework development platform. They are both developed, managed, and supported by the same language development team at Microsoft.[13] They compile to the same intermediate language (IL), which runs against the same .NET Framework runtime libraries.[14] Although there are some differences in the programming constructs, their differences are primarily syntactic and, assuming one avoids the Visual Basic "Compatibility" libraries provided by Microsoft to aid conversion from Visual Basic 6, almost every feature in VB has an equivalent feature in C# and vice versa. Lastly, both languages reference the same Base Classes of the .NET Framework to extend their functionality. As a result, with few exceptions, a program written in either language can be run through a simple syntax converter to translate to the other. There are many open source and commercially available products for this task.
Examples
Hello World!
Windows Forms Application

Requires a button called Button1.

Public Class Form1

    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        MsgBox("Hello world!", MsgBoxStyle.Information, "Hello world!") ' Show a message that says "Hello world!".
    End Sub
End Class

Hello world! window
Console Application

Module Module1

    Sub Main()
        Console.WriteLine("Hello world!") ' Write in the console "Hello world!" and start a new line.
        Console.ReadKey() ' The user must press any key before the application ends.
    End Sub
End Module

Speaking
Windows Forms Application

Requires a TextBox titled 'TextBox1' and a button called Button1.

Public Class Form1
    
    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        CreateObject("Sapi.Spvoice").Speak(TextBox1.Text)
    End Sub
End Class

Console Application

Module Module1
    Private Voice = CreateObject("Sapi.Spvoice")
    Private Text As String

    Sub Main()
        Console.Write("Enter the text to speak: ") ' Say "Enter the text to speak: "
        Text = Console.ReadLine() ' The user must enter the text to speak.
        Voice.Speak(Text) ' Speak the text the user has entered.
    End Sub
End Module

Version history
...

[Message clipped]  View entire message
Mail Delivery Subsystem
	
	Fri, Apr 5, 10:25 AM (6 days ago)
Address not found Your message wasn't delivered to tshigombekb@gmail.com because the address couldn't be found, or is unable to receive mail. LEARN MORE The res
tshingombe fiston <tshingombefiston@gmail.com>
	
Fri, Apr 5, 10:27 AM (6 days ago)
	
to TSHINGOMBEKB, tshigombekb, me
Main menu













Wikipedia The Free Encyclopedia

    Create account
    Log in 

Personal tools



Contents


    Dialects, flavors and implementations
    Classifications
    See also
    References
    Further reading

Programming language

    Article
    Talk

    Read
    Edit
    View history

Tools




















Page protected with pending changes
From Wikipedia, the free encyclopedia
The source code for a computer program in C. The gray lines are comments that explain the program to humans. When compiled and run, it will give the output "Hello, world!".

A programming language is a system of notation for writing computer programs.[1]

Programming languages are described in terms of their syntax (form) and semantics (meaning), usually defined by a formal language. Languages usually provide features such as a type system, variables and mechanisms for error handling. An implementation of a programming language in the form of a compiler or interpreter allows programs to be executed, either directly or by producing an executable.

Computer architecture has strongly influenced the design of programming languages, with the most common type (imperative languages—which implement operations in a specified order) developed to perform well on the popular von Neumann architecture. While early programming languages were closely tied to the hardware, over time, they have developed more abstraction to hide implementation details for greater simplicity.

Thousands of programming languages—often classified as imperative, functional, logic, or object-oriented—have been developed for a wide variety of uses. Many aspects of programming language design involve tradeoffs—for example, exception handling simplifies error handling, but at a performance cost. Programming language theory is the subfield of computer science that studies the design, implementation, analysis, characterization, and classification of programming languages.
Definitions

There are a variety of criteria that may be considered when defining what constitutes a programming language.
Computer languages vs programming languages

The term computer language is sometimes used interchangeably with programming language.[2] However, the usage of both terms varies among authors, including the exact scope of each. One usage describes programming languages as a subset of computer languages.[3] Similarly, languages used in computing that have a different goal than expressing computer programs are generically designated computer languages. For instance, markup languages are sometimes referred to as computer languages to emphasize that they are not meant to be used for programming.[4] One way of classifying computer languages is by the computations they are capable of expressing, as described by the theory of computation. The majority of practical programming languages are Turing complete,[5] and all Turing complete languages can implement the same set of algorithms. ANSI/ISO SQL-92 and Charity are examples of languages that are not Turing complete, yet are often called programming languages.[6][7] However, some authors restrict the term "programming language" to Turing complete languages.[1][8]

Another usage regards programming languages as theoretical constructs for programming abstract machines and computer languages as the subset thereof that runs on physical computers, which have finite hardware resources.[9] John C. Reynolds emphasizes that formal specification languages are just as much programming languages as are the languages intended for execution. He also argues that textual and even graphical input formats that affect the behavior of a computer are programming languages, despite the fact they are commonly not Turing-complete, and remarks that ignorance of programming language concepts is the reason for many flaws in input formats.[10]
Domain and target

In most practical contexts, a programming language involves a computer; consequently, programming languages are usually defined and studied this way.[11] Programming languages differ from natural languages in that natural languages are only used for interaction between people, while programming languages also allow humans to communicate instructions to machines.

The domain of the language is also worth consideration. Markup languages like XML, HTML, or troff, which define structured data, are not usually considered programming languages.[12][13][14] Programming languages may, however, share the syntax with markup languages if a computational semantics is defined. XSLT, for example, is a Turing complete language entirely using XML syntax.[15][16][17] Moreover, LaTeX, which is mostly used for structuring documents, also contains a Turing complete subset.[18][19]
Abstractions

Programming languages usually contain abstractions for defining and manipulating data structures or controlling the flow of execution. The practical necessity that a programming language supports adequate abstractions is expressed by the abstraction principle.[20] This principle is sometimes formulated as a recommendation to the programmer to make proper use of such abstractions.[21]
History
Early developments

The first programmable computers were invented at the end of the 1940s, and with them, the first programming languages.[22] The earliest computers were programmed in first-generation programming languages (1GLs), machine language (simple instructions that could be directly executed by the processor). This code was very difficult to debug and was not portable between different computer systems.[23] In order to improve the ease of programming, assembly languages (or second-generation programming languages—2GLs) were invented, diverging from the machine language to make programs easier to understand for humans, although they did not increase portability.[24]

Initially, hardware resources were scarce and expensive, while human resources were cheaper. Therefore, cumbersome languages that were time-consuming to use, but were closer to the hardware for higher efficiency were favored.[25] The introduction of high-level programming languages (third-generation programming languages—3GLs)—revolutionized programming. These languages abstracted away the details of the hardware, instead being designed to express algorithms that could be understood more easily by humans. For example, arithmetic expressions could now be written in symbolic notation and later translated into machine code that the hardware could execute.[24] In 1957, Fortran (FORmula TRANslation) was invented. Often considered the first compiled high-level programming language,[24][26] Fortran has remained in use into the twenty-first century.[27]
1960s and 1970s
Two people using an IBM 704 mainframe—the first hardware to support floating-point arithmetic—in 1957. Fortran was designed for this machine.[28][27]

Around 1960, the first mainframes—general purpose computers—were developed, although they could only be operated by professionals and the cost was extreme. The data and instructions were input by punch cards, meaning that no input could be added while the program was running. The languages developed at this time therefore are designed for minimal interaction.[29] After the invention of the microprocessor, computers in the 1970s became dramatically cheaper.[30] New computers also allowed more user interaction, which was supported by newer programming languages.[31]

Lisp, implemented in 1958, was the first functional programming language. Unlike Fortran, it supports recursion and conditional expressions,[32] and it also introduced dynamic memory management on a heap and automatic garbage collection.[33] For the next decades, Lisp dominated artificial intelligence applications.[34] In 1978, another functional language, ML, introduced inferred types and polymorphic parameters.[31][35]

After ALGOL (ALGOrithmic Language) was released in 1958 and 1960,[36] it became the standard in computing literature for describing algorithms. Although its commercial success was limited, most popular imperative languages—including C, Pascal, Ada, C++, Java, and C#—are directly or indirectly descended from ALGOL 60.[37][27] Among its innovations adopted by later programming languages included greater portability and the first use of context-free, BNF grammar.[38] Simula, the first language to support object-oriented programming (including subtypes, dynamic dispatch, and inheritance), also descends from ALGOL and achieved commercial success.[39] C, another ALGOL descendant, has sustained popularity into the twenty-first century. C allows access to lower-level machine operations more than other contemporary languages. Its power and efficiency, generated in part with flexible pointer operations, comes at the cost of making it more difficult to write correct code.[31]

Prolog, designed in 1972, was the first logic programming language, communicating with a computer using formal logic notation.[40][41] With logic programming, the programmer specifies a desired result and allows the interpreter to decide how to achieve it.[42][41]
1980s to 2000s
A small selection of programming language textbooks

During the 1980s, the invention of the personal computer transformed the roles for which programming languages were used.[43] New languages introduced in the 1980s included C++, a superset of C that can compile C programs but also supports classes and inheritance.[44] Ada and other new languages introduced support for concurrency.[45] The Japanese government invested heavily into the so-called fifth-generation languages that added support for concurrency to logic programming constructs, but these languages were outperformed by other concurrency-supporting languages.[46][47]

Due to the rapid growth of the Internet and the World Wide Web in the 1990s, new programming languages were introduced to support Web pages and networking.[48] Java, based on C++ and designed for increased portability across systems and security, enjoyed large-scale success because these features are essential for many Internet applications.[49][50] Another development was that of dynamically typed scripting languages—Python, JavaScript, PHP, and Ruby—designed to quickly produce small programs that coordinate existing applications. Due to their integration with HTML, they have also been used for building web pages hosted on servers.[51][52]
2000s to present

During the 2000s, there was a slowdown in the development of new programming languages that achieved widespread popularity.[53] One innovation was service-oriented programming, designed to exploit distributed systems whose components are connected by a network. Services are similar to objects in object-oriented programming, but run on a separate process.[54] C# and F# cross-pollinated ideas between imperative and functional programming.
...

[Message clipped]  View entire message
Mail Delivery Subsystem
	
	Fri, Apr 5, 10:27 AM (6 days ago)
Address not found Your message wasn't delivered to tshigombekb@gmail.com because the address couldn't be found, or is unable to receive mail. LEARN MORE The res
tshingombe fiston <tshingombefiston@gmail.com>
	
Fri, Apr 5, 10:31 AM (6 days ago)
	
to TSHINGOMBEKB, tshigombekb, me

    About Us
    Contact Us

TheDataLabs

    Home
    Python Tutorial
    MS Excel
    VBAPopular
    Dashboards
    Power BI
    Templates & TrackersNew
    Blogs

HomeTemplates & Trackers
Templates & TrackersBlogs
Automated Student’s Registration Form in Excel and VBA
S Tiwari
By S Tiwari
February 18, 2020
14 min.
Modified date: December 5, 2023
67743
8
Share
Form Form

This article is primarily focused on developing an Automated Student’s Registration applications using the Visual Basic for Applications (VBA) programming language. With Excel VBA you can create a user form to to automate the data entry task using what is called a macro.

Student’s registration form is just taken as example to develop the data entry form. Once you complete this article, you will be able to develop a data entry application with all required features.

In this article, you will learn:

    Create Home, Database and Support Sheet
    User Interface for Data Entry
    Import Custom Calendar and Icons
    Design Form and assign properties to all controls
    Code to Reset and Initialize the User Form
    Function to Validate Email ID and Other Inputs done by User
    Sub Procedure to Create a folder
    Procedure to upload the Passport Size Photo and Consolidate the pictures in folder
    Assign the path of uploaded pictures to Image Control
    Sub Procedure to Submit or Transfer the Data from user-form to database sheet
    Sub Procedure to Edit and Delete the existing records
    Assign the Macro to run the form

So in this article, a lot to know and a lot to cover. Please read this article carefully and follow the instructions to develop the Data Entry Form with Image.
Step 1 – Creating Excel File

    Open the Excel Application
    Create a New Blank Workbook
    Save the Excel file with the Name ‘Student Registration Form.xlsm’

Step 2 – Creating Home Sheet

    Add three new worksheets in this file
    Rename the first sheet to ‘Home’
    Format the sheets and add a Rounded Rectangle with caption as per below image

HomeHome
Step 3 – Creating Database Sheet and Columns

    Rename the second worksheets to ‘Database’
    Add the required columns in ‘Database’ worksheet
    Do the required formatting as per below image

DatabaseDatabase
Step 4 – Creating Support Sheet

    Rename the third worksheets to ‘Support’
    Add the Course details in Column A with column header ‘Courses’
    Apply the formatting as per below image

SupportSupport
Step 5 – Design the Data Entry Form in Visual Basic Environment window

    Insert a UserForm
    Design the Data Entry form as per below image

FormForm

3. Place all the Frames, Controls as per above image. Make sure we have utilized two hidden text-boxes to store row number and image path. Please create both the text box anywhere in the form. Details have been given in below mentioned properties.

Once you create controls with hidden text-boxes, set the Properties of Form and Controls as per below mentioned details.
UserForm Properties

Name: frmDataEntry
BackColor: &H00FFFFFF&
Caption : Student Registration Form
Height: 484
Width: 573
Frame1 – Frame1 and other controls properties

Name: Frame1
BackColor: &H8000000E&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Caption: Enter Details
Font: Tahoma, Regular, 12
ForeColor: &H00000080&
Height: 252
Width: 534
Controls in Frame1

Label Caption: Student’s Name

Control Type: TextBox
Name: txtStudentName
BackColor: &H80000005&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Font: Tahoma, Regular, 8
ForeColor: &H80000008&
Height: 20
Width: 192
TabIndex: 0

Label Caption: Father’s Name

Control Type: TextBox
Name: txtFatherName
BackColor: &H80000005&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Font: Tahoma, Regular, 8
ForeColor: &H80000008&
Height: 20
Width: 192
TabIndex: 1

Label Caption: Date Of Birth

Control Type: TextBox
Name: txtDOB
BackColor: &H80000005&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Font: Tahoma, Regular, 8
ForeColor: &H80000008&
Height: 20
Locked:True
Width: 192
TabIndex: 2

Icon for Calendar in Date of Birth Text Box

Control Type: Image
Name: imgCalendar
BackStyle: 0-frmBackStyleTransparent
BorderStyle: 0-frmBorderNone
Height: 20
PictureAlignment: 2-frmPictureAlignmentCenter
PictureSizeMode: 1-frmPictureSizeModeStretch
SpecialEffect: 0-frmSpecialEffectFlat
Width: 20

Label Caption: Gender

1. Control Type: Option Button
Name: optFemale
Caption: Female
Value:False
TabIndex: 3
2. Control Type: Option Button
Name: optMale
Caption: Male
Value:False
TabIndex: 4

Label Caption: Course Applied

Control Type: ComboBox
Name: cmbCourse
BackColor: &H80000005&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Font: Tahoma, Regular, 8
ForeColor: &H80000008&
Height: 20
Width: 192
TabIndex: 5

Label Caption: Mobile Number

Control Type: TextBox
Name: txtMobile
BackColor: &H80000005&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Font: Tahoma, Regular, 8
ForeColor: &H80000008&
Height: 20
Width: 192
TabIndex: 6

Label Caption: Email ID

Control Type: TextBox
Name: txtEmail
BackColor: &H80000005&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Font: Tahoma, Regular, 8
ForeColor: &H80000008&
Height: 20
Width: 192
TabIndex: 7

Hidden TextBox (to store row number – for internal purpose only)

Control Type: TextBox
Name: txtRowNumber
Visible: False

Image Control

Control Type: Image
Name: imgStudent
BackColor: &H80000005&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Height: 80
PictureAlignment: 2-frmPictureAlignmentCenter
PictureSizeMode: 1-frmPictureSizeModeStretch
SpecialEffect: 0-frmSpecialEffectFlat
Width: 80

Hidden TextBox (to store image path – for internal purpose only)

Control Type: TextBox
Name: txtImagePath
Visible: False

Command Button – To browse and upload the image

Control Type: CommandButton
Name: cmdLoadImage
BackColor: &H80000005&
Caption: Upload Image…
Font: Tahoma, Regular, 8
TabIndex: 9

Label Caption: Address :

Control Type: TextBox
Name: txtAddress
BackColor: &H80000005&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Font: Tahoma, Regular, 8
ForeColor: &H80000008&
Height: 63
MultiLine: True
ScrollBars: 2-frmScrollBarsVertical
TabIndex: 10
Width: 192

Command Button – Submit and Reset

Control Type: CommandButton
Name: cmdSubmit
Accelerator: s
BackColor: &H80000005&
Caption: Submit
Font: Tahoma, Regular, 9
Height: 20
TabIndex: 11
Width:60

Control Type: CommandButton
Name: cmdReset
Accelerator: r
BackColor: &H00FFC0FF&
Caption: Reset
Font: Tahoma, Regular, 9
Height: 20
TabIndex: 12
Width:60
Frame2 – Frame2 and other controls properties

Name: Frame2
BackColor: &H8000000E&
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Caption: Database
Font: Tahoma, Regular, 12
ForeColor: &H00000080&
Height: 186
Width: 534

Command Button – Edit and Delete

Control Type: CommandButton
Name: cmdEdit
Accelerator: e
BackColor: &H00FFC0C0&
Caption: Edit
Font: Tahoma, Regular, 9
Height: 20
TabIndex: 1
Width:60

Control Type: CommandButton
Name: cmdDelete
Accelerator: d
BackColor: &H00C0E0FF&
Caption: Delete
Font: Tahoma, Regular, 9
Height: 20
TabIndex: 2
Width:60

List-box to Show the Data

Control Type: ListBox
Name: lstDatabase
BorderColor: &H00000080&
BorderStyle: 1-frmBorderStyleSingle
Font: Tahoma, Regular, 8
ForeColor: &H80000008&
Height: 137
TabIndex: 0
Width:517

Now, we have prepare the Form, created required controls and set the properties as given below. Let’s move to the next step.

4. Import the MyCalendar custom calendar control from the Support Folder.

5. Insert a new module. To insert click on Insert Menu – > Module.

6. Change the name of Module1 to mdDataEntry in properties window.

7. Add the below mentioned code on Double Click event of txtDOB to show the Calendar and pick the DOB from custom calendar control.

Private Sub txtDOB_DblClick(ByVal Cancel As MSForms.ReturnBoolean)
Application.ScreenUpdating = False

Dim sDate As String

On Error Resume Next

sDate = MyCalendar.DatePicker(Me.txtDOB)

Me.txtDOB.Value = Format(sDate, "dd-mmm-yyyy")

On Error GoTo 0

Application.ScreenUpdating = True
End Sub

8. Add the below mentioned code on Click event of imgCalendar to show the Calendar and pick the DOB from custom calendar control.

Private Sub imgCalendar_Click()

Application.ScreenUpdating = False

Dim sDate As String

On Error Resume Next

sDate = MyCalendar.DatePicker(Me.txtDOB)

Me.txtDOB.Value = Format(sDate, "dd-mmm-yyyy")

On Error GoTo 0

Application.ScreenUpdating = True
End Sub

9. Let’s double click on mdDataEntry module and add the code to perform Reset, Validate, Load Image, Transfer, Edit, Delete and others.
Code to Reset and Initialize the form with default value

Sub Reset_Form()
Dim iRow As Long

With frmDataEntry

    .txtStudentName.Text = ""
    .txtStudentName.BackColor = vbWhite

    .txtFatherName.Text = ""
    .txtFatherName.BackColor = vbWhite

    .txtDOB.Text = ""
    .txtDOB.BackColor = vbWhite

    .optFemale.Value = False
    .optMale.Value = False

    .txtMobile.Value = ""
    .txtMobile.BackColor = vbWhite

    .txtEmail.Value = ""
    .txtEmail.BackColor = vbWhite

    .txtAddress.Value = ""
    .txtAddress.BackColor = vbWhite

    .txtRowNumber.Value = ""
    .txtImagePath.Value = ""

    .imgStudent.Picture = LoadPicture(vbNullString)

    .cmdSubmit.Caption = "Submit"

    '.cmbCourse.Clear
    .cmbCourse.BackColor = vbWhite

    'Dynamic range based on Support Sheet
    shSupport.Range("A2", shSupport.Range("A" & Rows.Count).End(xlUp)).Name = "Dynamic"

    .cmbCourse.RowSource = "Dynamic"

    .cmbCourse.Value = ""

    .cmbCourse.Value = ""

    'Assigning RowSource to lstDatabase

    .lstDatabase.ColumnCount = 12
    .lstDatabase.ColumnHeads = True

    .lstDatabase.ColumnWidths = "30,70,70,40,45,70,60,60,70,0,0,0"

    iRow = shDatabase.Range("A" & Rows.Count).End(xlUp).row + 1 ' Identify last blank row

    If iRow > 1 Then

        .lstDatabase.RowSource = "Database!A2:L" & iRow

    Else

        .lstDatabase.RowSource = "Database!A2:L2"

    End If


End With
End Sub

Code to Validate the structure of email entered by user

Function ValidEmail(email As String) As Boolean 

 '   A regular expression is a pattern made up of a sequence of characters
 '    that you can use to find a matching pattern in another string.
 '    In order to use Regex in VBA you have to use the RegExp object.
 '    A pattern such as [A-C] can be used to search for and match an
 '    upper case letter from A to C from a sequence.

 Dim oRegEx As Object
 Set oRegEx = CreateObject("VBScript.RegExp")
 With oRegEx
    .Pattern = "^[\w-\.]{1,}\@([\da-zA-Z-]{1,}\.){1,}[\da-zA-Z-]{2,3}$"
    ValidEmail = .Test(email)
 End With
 Set oRegEx = Nothing
End Function

Function to Browse and Select the Image

Function GetImagePath() As String
GetImagePath = ""

With Application.FileDialog(msoFileDialogFilePicker) ' File Picker Dialog box

    .AllowMultiSelect = False
    .Filters.Clear      ' Clear the exisiting filters
    .Filters.Add "Images", "*.gif; *.jpg; *.jpeg" 'Add a filter that includes GIF and JPEG images

    ' show the file picker dialog box
    If .Show <> 0 Then

        GetImagePath = .SelectedItems(1) ' Getting the path of selected file name

    End If

End With
End Function

Sub Procedure to create a folder named ‘Images’ at the same location where Excel Files has been saved.

Sub CreateFolder()
Dim strFolder As String ' To hold the folter path where we need to replicate the image

strFolder = ThisWorkbook.Path & Application.PathSeparator & "Images"
'Check Directory exist or not. If not exist then it will return blank
     If Dir(strFolder, vbDirectory) = "" Then
         MkDir strFolder ' Make a folder with the name of 'Images'
     End If
End Sub

Sub Procedure to Save the selected image in Images folder and load it to Image control imgStudent

Sub LoadImange()
Dim imgSourcePath As String ' To store the path of image selected by user
Dim imgDestination As String ' To store the path of image selected by user

imgSourcePath = Trim(GetImagePath()) ' Call the Function

If imgSourcePath = "" Then Exit Sub

Call CreateFolder   'Create Image folder if not exist

imgDestination = ThisWorkbook.Path & Application.PathSeparator & _
frmDataEntry.txtStudentName & "." & Split(imgSourcePath, ".")(UBound(Split(imgSourcePath, ".")))

FileCopy imgSourcePath, imgDestination ' Code to copy image

frmDataEntry.imgStudent.PictureSizeMode = fmPictureSizeModeStretch 'Stretch mode
frmDataEntry.imgStudent.Picture = LoadPicture(imgDestination) ' Loading picture to imgStudent
frmDataEntry.txtImagePath.Value = imgDestination ' Assigning the path to text box
End Sub

Function to Validate data entered by user

Function ValidEntry() As Boolean

ValidEntry = True

With frmDataEntry

    'Default Color

    .txtStudentName.BackColor = vbWhite
    .txtFatherName.BackColor = vbWhite
    .txtDOB.BackColor = vbWhite
    .txtMobile.BackColor = vbWhite
    .txtEmail.BackColor = vbWhite
    .txtAddress.BackColor = vbWhite
    .cmbCourse.BackColor = vbWhite

    'Validating Student Name

    If Trim(.txtStudentName.Value) = "" Then
        MsgBox "Please enter Student's name.", vbOKOnly + vbInformation, "Student Name"
        .txtStudentName.BackColor = vbRed
        .txtStudentName.SetFocus
        ValidEntry = False
        Exit Function
    End If


    'Validating Father's name

    If Trim(.txtFatherName.Value) = "" Then
        MsgBox "Please enter Father's name.", vbOKOnly + vbInformation, "Father Name"
        .txtFatherName.BackColor = vbRed
        .txtFatherName.SetFocus
        ValidEntry = False
        Exit Function
    End If

    'Validating DOB

    If Trim(.txtDOB.Value) = "" Then
        MsgBox "DOB is blank. Please enter DOB.", vbOKOnly + vbInformation, "Invalid Entry"
        .txtDOB.BackColor = vbRed
        ValidEntry = False
        Exit Function
    End If


    'Validating Gender

    If .optFemale.Value = False And .optMale.Value = False Then
        MsgBox "Please select gender.", vbOKOnly + vbInformation, "Invalid Entry"
        ValidEntry = False
        Exit Function
    End If

    'Validating Course

    If Trim(.cmbCourse.Value) = "" Then
        MsgBox "Please select the Course from drop-down.", vbOKOnly + vbInformation, "Course Applied"
        .cmbCourse.BackColor = vbRed
        ValidEntry = False
        Exit Function
    End If

    'Validating Mobile Number

    If Trim(.txtMobile.Value) = "" Or Len(.txtMobile.Value) < 10 Or Not IsNumeric(.txtMobile.Value) Then
        MsgBox "Please enter a valid mobile number.", vbOKOnly + vbInformation, "Invalid Entry"
        .txtMobile.BackColor = vbRed
        .txtMobile.SetFocus
        ValidEntry = False
        Exit Function
    End If

    'Validating Email

    If ValidEmail(Trim(.txtEmail.Value)) = False Then
        MsgBox "Please enter a valid email address.", vbOKOnly + vbInformation, "Invalid Entry"
        .txtEmail.BackColor = vbRed
        .txtEmail.SetFocus
        ValidEntry = False
        Exit Function
    End If

    'Validating Address

    If Trim(.txtAddress.Value) = "" Then
        MsgBox "Address is blank. Please enter a valid address.", vbOKOnly + vbInformation, "Invalid Entry"
        .txtAddress.BackColor = vbRed
        ValidEntry = False
        Exit Function
    End If

    'Validating Image

    If .imgStudent.Picture Is Nothing Then
       MsgBox "Please upload the PP Size Photo.", vbOKOnly + vbInformation, "Picture"
        ValidEntry = False
        Exit Function
    End If

End With
End Function

Sub Procedure to Transfer the Data from Form to Database sheet

Sub Submit_Data()
Dim iRow As Long

If frmDataEntry.txtRowNumber.Value = "" Then
   
 iRow = shDatabase.Range("A" & Rows.Count).End(xlUp).row + 1 ' Identify last blank row

Else
    iRow = frmDataEntry.txtRowNumber.Value

End If

With shDatabase.Range("A" & iRow)

.Offset(0, 0).Value = "=Row()-1" 'S. No.

.Offset(0, 1).Value = frmDataEntry.txtStudentName.Value 'Student's Name

.Offset(0, 2).Value = frmDataEntry.txtFatherName.Value    'Father's Name

.Offset(0, 3).Value = frmDataEntry.txtDOB.Value   'DOB

.Offset(0, 4).Value = IIf(frmDataEntry.optFemale.Value = True, "Female", "Male")  'Gender

.Offset(0, 5).Value = frmDataEntry.cmbCourse.Value    'Qualification

.Offset(0, 6).Value = frmDataEntry.txtMobile.Value    'Mobile Number

.Offset(0, 7).Value = frmDataEntry.txtEmail.Value     'Email

.Offset(0, 8).Value = frmDataEntry.txtAddress.Value   'Address

.Offset(0, 9).Value = frmDataEntry.txtImagePath.Value   'Photo

.Offset(0, 10).Value = Application.UserName    'Submitted By

.Offset(0, 11).Value = Format([Now()], "DD-MMM-YYYY HH:MM:SS")   'Submitted On

'Reset the form

Call Reset_Form

Application.ScreenUpdating = True

MsgBox "Data submitted successfully!"
End Sub

Function to find the selection in lstDatabase

Function Selected_List() As Long
Dim i As Long
Selected_List = 0
If frmDataEntry.lstDatabase.ListCount = 1 Then Exit Function ' If no items exist in List Box
For i = 0 To frmDataEntry.lstDatabase.ListCount - 1
If frmDataEntry.lstDatabase.Selected(i) = True Then
   Selected_List = i + 1
   Exit For
End If
Next i
End Function

Sub Procedure to Show the Form

Sub Show_Form()
frmDataEntry.Show
End Sub

Now, we have created all the Sub Procedures and Functions. Let’s call these functions and procedures on click events and form intilization.

Go to Form and double click on ‘cmdLoadImage’ command button to call the ‘LoadImage’ sub procedure.

Private Sub cmdLoadImage_Click()
If Me.txtStudentName.Value = "" Then
 MsgBox "Please enter Student's first.", vbOKOnly + vbCritical, "Error"
 Exit Sub
End If

Call LoadImange
End Sub

Call the Reset_Form sub-procedure on Form Initialization

Private Sub UserForm_Initialize()
Call Reset_Form
End Sub

Assign the code on Click event of Submit Button

Private Sub cmdSubmit_Click()
Dim i As VbMsgBoxResult

i = MsgBox("Do you want to submit the data?", vbYesNo + vbQuestion, "Submit Data")

If i = vbNo Then Exit Sub

If ValidEntry Then

    Call Submit_Data

End If
End Sub

Assign the code on Click event of Reset Button

Private Sub cmdReset_Click()
Dim i As VbMsgBoxResult

i = MsgBox("Do you want to reset the form?", vbYesNo + vbQuestion, "Reset")

If i = vbNo Then Exit Sub

Call Reset_Form
End Sub

Add the below code on double click of lstDatabase to edit the record

Private Sub lstDatabase_DblClick(ByVal Cancel As MSForms.ReturnBoolean)

If Selected_List = 0 Then
     MsgBox "No row is selected.", vbOKOnly + vbInformation, "Edit"
     Exit Sub
End If

Dim sGender As String

'Me.txtRowNumber = Selected_List + 1 ' Assigning Selected Row Number of Database Sheet

Me.txtRowNumber = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 0) + 1

'Assigning the Selected Reocords to Form controls

frmDataEntry.txtStudentName.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 1)

frmDataEntry.txtFatherName.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 2)

frmDataEntry.txtDOB.Value = Format(Me.lstDatabase.List(Me.lstDatabase.ListIndex, 3), "dd-mmm-yyyy")

sGender = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 4)

If sGender = "Female" Then
    frmDataEntry.optFemale.Value = True
Else
    frmDataEntry.optMale.Value = True
End If

frmDataEntry.cmbCourse.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 5)
frmDataEntry.txtMobile.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 6)
frmDataEntry.txtEmail.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 7)
frmDataEntry.txtAddress.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 8)
frmDataEntry.imgStudent.Picture = LoadPicture(Me.lstDatabase.List(Me.lstDatabase.ListIndex, 9))
frmDataEntry.txtImagePath = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 9)
Me.cmdSubmit.Caption = "Update"
MsgBox "Please make the required changes and Click on Update."
End Sub

Write the below code on click event of cmdDelete command button

Private Sub cmdDelete_Click()
If Selected_List = 0 Then

     MsgBox "No row is selected.", vbOKOnly + vbInformation, "Delete"
     Exit Sub

End If

Dim i As VbMsgBoxResult

Dim row As Long

row = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 0) + 1

i = MsgBox("Do you want ot delete the selected record?", vbYesNo + vbQuestion, "Delete")

If i = vbNo Then Exit Sub

ThisWorkbook.Sheets("Database").Rows(row).Delete

Call Reset ' Refresh the controls with latest information

MsgBox "Selected record has been successfully deleted.", vbOKOnly + vbInformation, "Delete"
End Sub

Write the below code on click event of cmdEdit command button

Private Sub cmdEdit_Click()
If Selected_List = 0 Then

     MsgBox "No row is selected.", vbOKOnly + vbInformation, "Edit"
     Exit Sub

End If

Dim sGender As String

Me.txtRowNumber = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 0) + 1

'Assigning the Selected Reocords to Form controls

frmDataEntry.txtStudentName.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 1)

frmDataEntry.txtFatherName.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 2)

frmDataEntry.txtDOB.Value = Format(Me.lstDatabase.List(Me.lstDatabase.ListIndex, 3), "dd-mmm-yyyy")

sGender = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 4)

If sGender = "Female" Then
    frmDataEntry.optFemale.Value = True
Else
    frmDataEntry.optMale.Value = True
End If
frmDataEntry.cmbCourse.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 5)
frmDataEntry.txtMobile.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 6)
frmDataEntry.txtEmail.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 7)
frmDataEntry.txtAddress.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 8)
frmDataEntry.imgStudent.Picture = LoadPicture(Me.lstDatabase.List(Me.lstDatabase.ListIndex, 9))
frmDataEntry.txtImagePath = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 9)
Me.cmdSubmit.Caption = "Update"
MsgBox "Please make the required changes and Click on Update."
End Sub

Now, we have successfully assigned and called all the required functions and procedures on different events. Let’s move ‘Home’ sheet in Excel and assign the macro ‘Show_Form’ on rectangular button so that user can click there to launch the form.

Student’s Registration Form is ready. You can test this form and start using.

Please watch the Step by Step Tutorial on YouTube.

Please download the Support and Excel file used in this tutorial.
DownloadClick to download

Thanks!

    DownloadFemaleStoresFree DownloadsDigital picture frameLearn

    AcceleratorAutomateBasic VisualBasicsDownloadFemaleStores

    Tags
    Data Entry Form
    Data Entry form with Image and ListBox
    Data Entry Tool
    Data Entry with Image
    Dynamic Drop-down in VBA
    Edit and Delete in Form
    Form with Image control
    Image
    Load Image in VBA
    Store Image in Excel
    Store Imange in VBA

Share
Copy URL
Previous article
How to learn Excel VBA 2019?
Next article
Automated Data Collator in Excel
8 COMMENTS

    jony jony February 19, 2020 At 19:19

    Automated Student’s Registration Form in Excel and VBA download button not work.
    Reply
    Waseem Akram Waseem Akram February 29, 2020 At 11:24

    Dear Please send me this file
    Reply
        TheDataLabs TheDataLabs June 1, 2020 At 12:36

        Please download it from the link provided in this post. Thanks!
        Reply
    Sivabalan Sivabalan March 13, 2020 At 23:53

    Brother, It is amazing
    Reply
        TheDataLabs TheDataLabs June 1, 2020 At 12:35

        Thanks for your feedback!
        Reply
    Erik Santos Erik Santos April 27, 2020 At 08:31

    Thanks for sharing the knowledge

    I made a small correction to your code and it works perfectly.

    lstDatabase.ColumnWidths = “20 pt;85 pt;85 pt;65 pt;50 pt;60 pt;65 pt;60 pt;0 pt;0 pt;0 pt;0 pt”
    Reply
    Israel Adeyemi Israel Adeyemi December 17, 2021 At 16:35

    Good job. this is an excellent class
    Reply
    출장마사지 출장마사지 March 3, 2023 At 22:09

    Amazing things here. I’m very happy to look your post. Thank you so
    much and I am looking forward to contact you. Will you please drop me a mail?
    Reply

LEAVE A REPLY
Comment:
Name:*
Email:*
Website:

Save my name, email, and website in this browser for the next time I comment.

Recommended Reads
Easy-To-Follow: Create a Fully Automated Data Entry Userform in Excel and VBA in 5 Easy Steps
December 7, 2023
How To Create an Automated Data Entry Form in Google Sheets: A Step-by-Step Easy Guide (2023)
December 7, 2023
Advance Data Entry Form
December 5, 2023
Data Entry Form
December 5, 2023
Automated NSE Option Chain Data Extractor
December 5, 2023
Popular Categories

    Blogs73
    Templates & Trackers31
    MS Excel & VBA20
    Excel Tips and Tricks11
    Charts and Visualization10
    VBA Programming10
    Utility Tools9
    VBA Code Samples7

Latest Articles
Python Introduction
March 29, 2024
Call Center Performance Dashboard in Excel
Unlock Efficiency: # 1 Call Center Performance Dashboard in Excel (Free...
March 14, 2024
Comparative Sales Analysis
Mastering Comparative Sales Analysis – Sales vs. Target Dashboard in Microsoft...
March 14, 2024
Load more
Subscribe to stay informed

Stay in the loop with TheDataLabs by subscribing to our newsletter. Receive updates right in your inbox and never miss a thing!
TheDataLabs
About Us

We are dedicated to support the professional community through our experience sharing in Excel, VBA, Dashboard creation, Report generation and Automation techniques. Everything we offer here is freely available, and we DON'T ENGAGE in any paid training or services. 
Categories
Blogs73Charts and Visualization10Complaint Management System0Dashboard & Report1Data Entry Form1Data Modeling0
Free Downloads

    Utility Tools
    VBA Code Samples

Archives

    March 2024
    December 2023
    October 2023
    July 2023
    June 2023
    May 2023

© 2016-2024 TheDataLabs™ - Privacy Policy | Terms and Conditions
...

[Message clipped]  View entire message
Mail Delivery Subsystem
	
	Fri, Apr 5, 10:32 AM (6 days ago)
Address not found Your message wasn't delivered to tshigombekb@gmail.com because the address couldn't be found, or is unable to receive mail. LEARN MORE The res
tshingombe fiston <tshingombefiston@gmail.com>
	
AttachmentsFri, Apr 5, 11:09 AM (6 days ago)
	
to TSHINGOMBEKB, tshigombekb, me
...

[Message clipped]  View entire message
 3 Attachments  •  Scanned by Gmail
Mail Delivery Subsystem
	
	Fri, Apr 5, 11:09 AM (6 days ago)
Address not found Your message wasn't delivered to tshigombekb@gmail.com because the address couldn't be found, or is unable to receive mail. LEARN MORE The res
tshingombe fiston <tshingombefiston@gmail.com>
	
Fri, Apr 5, 11:17 AM (6 days ago)
	
to TSHINGOMBEKB, tshigombekb, me
Private Sub Frame1_Click()

End Sub

Private Sub Frame3_Click()

End Sub

Private Sub Label7_Click()

End Sub

Private Sub Label8_Click()

End Sub

Private Sub ListBox1_Click()

End Sub

Private Sub ListBox2_Click()

End Sub

Private Sub ListBox3_Click()

End Sub

Private Sub ListBox4_Click()

End Sub

Private Sub ListBox5_Click()

End Sub

Private Sub ListBox6_Click()

End Sub

Private Sub OptionButton1_Click()

End Sub

Private Sub OptionButton2_Click()

End Sub

Private Sub TextBox1_Change()

End Sub

Private Sub UserForm_Click()

End Sub

Private Sub UserForm_DblClick(ByVal Cancel As MSForms.ReturnBoolean)

End Sub

Private Sub UserForm_Error(ByVal Number As Integer, ByVal Description As MSForms.ReturnString, ByVal SCode As Long, ByVal Source As String, ByVal HelpFile As String, ByVal HelpContext As Long, ByVal CancelDisplay As MSForms.ReturnBoolean)

End Sub

Private Sub UserForm_KeyUp(ByVal KeyCode As MSForms.ReturnInteger, ByVal Shift As Integer)

End Sub

Private Sub UserForm_MouseUp(ByVal Button As Integer, ByVal Shift As Integer, ByVal X As Single, ByVal Y As Single)

End Sub

Private Sub UserForm_QueryClose(Cancel As Integer, CloseMode As Integer)

End Sub

Private Sub UserForm_RemoveControl(ByVal Control As MSForms.Control)

End Sub

Private Sub UserForm_Resize()

End Sub

Private Sub UserForm_Scroll(ByVal ActionX As MSForms.fmScrollAction, ByVal ActionY As MSForms.fmScrollAction, ByVal RequestDx As Single, ByVal RequestDy As Single, ByVal ActualDx As MSForms.ReturnSingle, ByVal ActualDy As MSForms.ReturnSingle)

End Sub

Private Sub UserForm_Terminate()

End Sub

Private Sub UserForm_Zoom(Percent As Integer)



End Sub
    'Assigning RowSource to lstDatabase

    .lstDatabase.ColumnCount = 12
    .lstDatabase.ColumnHeads = True

    .lstDatabase.ColumnWidths = "30,70,70,40,45,70,60,60,70,0,0,0"

    iRow = shDatabase.Range("A" & Rows.Count).End(xlUp).row + 1 ' Identify last blank row

    If iRow > 1 Then

        .lstDatabase.RowSource = "Database!A2:L" & iRow

    Else

        .lstDatabase.RowSource = "Database!A2:L2"

    End If


End With
End Sub



Function ValidEmail(email As String) As Boolean

 '   A regular expression is a pattern made up of a sequence of characters
 '    that you can use to find a matching pattern in another string.
 '    In order to use Regex in VBA you have to use the RegExp object.
 '    A pattern such as [A-C] can be used to search for and match an
 '    upper case letter from A to C from a sequence.

 Dim oRegEx As Object
 Set oRegEx = CreateObject("VBScript.RegExp")
 With oRegEx
    .Pattern = "^[\w-\.]{1,}\@([\da-zA-Z-]{1,}\.){1,}[\da-zA-Z-]{2,3}$"
    ValidEmail = .Test(email)
 End With
 Set oRegEx = Nothing
End Function



Function GetImagePath() As String
GetImagePath = ""

With Application.FileDialog(msoFileDialogFilePicker) ' File Picker Dialog box

    .AllowMultiSelect = False
    .Filters.Clear      ' Clear the exisiting filters
    .Filters.Add "Images", "*.gif; *.jpg; *.jpeg" 'Add a filter that includes GIF and JPEG images

    ' show the file picker dialog box
    If .Show <> 0 Then

        GetImagePath = .SelectedItems(1) ' Getting the path of selected file name

    End If

End With
End Function



Sub CreateFolder()
Dim strFolder As String ' To hold the folter path where we need to replicate the image

strFolder = ThisWorkbook.Path & Application.PathSeparator & "Images"
'Check Directory exist or not. If not exist then it will return blank
     If Dir(strFolder, vbDirectory) = "" Then
         MkDir strFolder ' Make a folder with the name of 'Images'
     End If
End Sub



Sub LoadImange()
Dim imgSourcePath As String ' To store the path of image selected by user
Dim imgDestination As String ' To store the path of image selected by user

imgSourcePath = Trim(GetImagePath()) ' Call the Function

If imgSourcePath = "" Then Exit Sub

Call CreateFolder   'Create Image folder if not exist

imgDestination = ThisWorkbook.Path & Application.PathSeparator & _
frmDataEntry.txtStudentName & "." & Split(imgSourcePath, ".")(UBound(Split(imgSourcePath, ".")))

FileCopy imgSourcePath, imgDestination ' Code to copy image

frmDataEntry.imgStudent.PictureSizeMode = fmPictureSizeModeStretch 'Stretch mode
frmDataEntry.imgStudent.Picture = LoadPicture(imgDestination) ' Loading picture to imgStudent
frmDataEntry.txtImagePath.Value = imgDestination ' Assigning the path to text box
End Sub


Value)) = False Then
Value = "" Then
Value
Value 'Student's Name

.Offset(0, 2).Value = frmDataEntry.txtFatherName.Value    'Father's Name
Value = True, "Female", "Male")  'Gender
Value   'Photo
Function Selected_List() As Long
Dim i As Long
Selected_List = 0
If frmDataEntry.lstDatabase.ListCount = 1 Then Exit Function ' If no items exist in List Box
For i = 0 To frmDataEntry.lstDatabase.ListCount - 1
If frmDataEntry.lstDatabase.Selected(i) = True Then
   Selected_List = i + 1
   Exit For
End If
Next i
End Function



Sub Show_Form()
frmDataEntry.Show
End Sub


Private Sub cmdLoadImage_Click()
If Me.txtStudentName.Value = "" Then
 MsgBox "Please enter Student's first.", vbOKOnly + vbCritical, "Error"
 Exit Sub
End If

Call LoadImange
End Sub



Private Sub UserForm_Initialize()
Call Reset_Form
End Sub



Private Sub cmdSubmit_Click()
Dim i As VbMsgBoxResult

i = MsgBox("Do you want to submit the data?", vbYesNo + vbQuestion, "Submit Data")

If i = vbNo Then Exit Sub

If ValidEntry Then

    Call Submit_Data

End If
End Sub


Private Sub cmdReset_Click()
Dim i As VbMsgBoxResult

i = MsgBox("Do you want to reset the form?", vbYesNo + vbQuestion, "Reset")

If i = vbNo Then Exit Sub

Call Reset_Form
End Sub



lstDatabase.ListIndex, 0) + 1
Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 1)

frmDataEntry.txtFatherName.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 2)

frmDataEntry.txtDOB.Value = Format(Me.lstDatabase.List(Me.lstDatabase.ListIndex, 3), "dd-mmm-yyyy")

sGender = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 4)
lstDatabase.ListIndex, 5)
frmDataEntry.txtMobile.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 6)
frmDataEntry.txtEmail.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 7)
frmDataEntry.txtAddress.Value = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 8)
frmDataEntry.imgStudent.Picture = LoadPicture(Me.lstDatabase.List(Me.lstDatabase.ListIndex, 9))
frmDataEntry.txtImagePath = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 9)
Private Sub cmdDelete_Click()
If Selected_List = 0 Then

     MsgBox "No row is selected.", vbOKOnly + vbInformation, "Delete"
     Exit Sub

End If

Dim i As VbMsgBoxResult

Dim row As Long

row = Me.lstDatabase.List(Me.lstDatabase.ListIndex, 0) + 1

i = MsgBox("Do you want ot delete the selected record?", vbYesNo + vbQuestion, "Delete")

If i = vbNo Then Exit Sub

ThisWorkbook.Sheets("Database").Rows(row).Delete

Call Reset ' Refresh the controls with latest information

MsgBox "Selected record has been successfully deleted.", vbOKOnly + vbInformation, "Delete"
End Sub



...

[Message clipped]  View entire message
Mail Delivery Subsystem
	
	Fri, Apr 5, 11:17 AM (6 days ago)
Address not found Your message wasn't delivered to tshigombekb@gmail.com because the address couldn't be found, or is unable to receive mail. LEARN MORE The res
tshingombe fiston <tshingombefiston@gmail.com>
	
Fri, Apr 5, 11:30 AM (6 days ago)
	
to TSHINGOMBEKB, tshigombekb, me
Commit
Update codeql.yml emgi registra exc

excell

    main

@t5h2i0tadi
t5h2i0tadi committed Apr 5, 2024
1 parent d3c290a commit 377ac51
Showing 1 changed file with 565 additions and 1 deletion.



566 changes: 565 additions & 1 deletion 566 .github/workflows/codeql.yml
@@ -81,4 +81,568 @@ jobs:
- name: Perform CodeQL Analysis
- name: Perform CodeQL Analysis
uses: github/codeql-action/analyze@v3
uses: github/codeql-action/analyze@v3
with:
with:
category: "/language:${{matrix.language}}"
category: "/language:${{matrix.language}}"Private Sub Frame1_Click()
<table class="gmail-diff-table gmail-js-diff-tabl
...

[Message clipped]  View entire message
Mail Delivery Subsystem
	
Fri, Apr 5, 11:30 AM (6 days ago)
	
to me
Error Icon
Address not found
Your message wasn't delivered to tshigombekb@gmail.com because the address couldn't be found, or is unable to receive mail.
LEARN MORE
The response was:

550 5.1.1 The email account that you tried to reach does not exist. Please try double-checking the recipient's email address for typos or unnecessary spaces. For more information, go to https://support.google.com/mail/?p=NoSuchUser s11-20020a056512214b00b00514c825ec93sor282071lfr.4 - gsmtp
tshingombe fiston <tshingombefiston@gmail.com>
	
AttachmentsFri, Apr 5, 11:31 AM (6 days ago)
	
to TSHINGOMBEKB, tshigombekb, me

    'Validating Gender



    If .optFemale.Value = False And .optMale.Value = False Then

    MsgBox "Please select gender.", vbOKOnly + vbInformation, "Invalid Entry"

    ValidEntry = False

    Exit Function

    End If



    'Validating Course



    If Trim(.cmbCourse.Value) = "" Then

    MsgBox "Please select the Course from drop-down.", vbOKOnly + vbInformation, "Course Applied"

    .cmbCourse.BackColor = vbRed

    ValidEntry = False

    Exit Function

    End If



    'Validating Mobile Number



    If Trim(.txtMobile.Value) = "" Or Len(.txtMobile.Value) < 10 Or Not IsNumeric(.txtMobile.Value) Then

    MsgBox "Please enter a valid mobile number.", vbOKOnly + vbInformation, "Invalid Entry"

    .txtMobile.BackColor = vbRed

    .txtMobile.SetFocus

    ValidEntry = False

    Exit Function

    End If



    'Validating Email



    If ValidEmail(Trim(.txtEmail.Value)) = False Then

    MsgBox "Please enter a valid email address.", vbOKOnly + vbInformation, "Invalid Entry"

    .txtEmail.BackColor = vbRed

    .txtEmail.SetFocus

    ValidEntry = False

    Exit Function

    End If



    'Validating Address



    If Trim(.txtAddress.Value) = "" Then

    MsgBox "Address is blank. Please enter a valid address.", vbOKOnly + vbInformation, "Invalid Entry"

    .txtAddress.BackColor = vbRed

    ValidEntry = False

    Exit Function

    End If



    'Validating Image



    If .imgStudent.Picture Is Nothing Then

    MsgBox "Please upload the PP Size Photo.", vbOKOnly + vbInformation, "Picture"

    ValidEntry = False

    Exit Function

    End If



    End With

    End Function





    Sub Submit_Data()

    Dim iRow As Long



    If frmDataEntry.txtRowNumber.Value = "" Then



    iRow = shDatabase.Range("A" & Rows.Count).End(xlUp).row + 1 ' Identify last blank row



...

[Message clipped]  View entire message
 7 Attachments  •  Scanned by Gmail
Mail Delivery Subsystem
	
Fri, Apr 5, 11:31 AM (6 days ago)
	
to me
Error Icon
Address not found
Your message wasn't delivered to tshigombekb@gmail.com because the address couldn't be found, or is unable to receive mail.
LEARN MORE
The response was:

550 5.1.1 The email account that you tried to reach does not exist. Please try double-checking the recipient's email address for typos or unnecessary spaces. For more information, go to https://support.google.com/mail/?p=NoSuchUser c23-20020ac25317000000b00516cb3a20c2sor289271lfh.1 - gsmtp
	
Page 1 of 28
