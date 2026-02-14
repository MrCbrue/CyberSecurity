# Easy Peasy Crackme

2/13/2026

This is a crack me I found at https://crackmes.one/crackme/5d295dde33c5d410dc4d0d05. This is supposed to be very easy, as the name suggests. I will be using Ghidra to examine this file. The username and password are changed (aka not the actual password).

## Decompiled Main Function

int __cdecl .text(int _Argc,char **_Argv,char **_Env)

{
  longlong *plVar1;
  undefined8 uVar2;
  string local_58 [16];
  string local_48 [16];
  string local_38 [16];
  string local_28 [24];
  
  __main();
  std::allocator<char>::allocator();
  std::string::string(local_28,"EXAMPLEUSERNAME");
  std::allocator<char>::~allocator();
  std::allocator<char>::allocator();
  std::string::string(local_38,"EXAMPLEPASSWORD");
  std::allocator<char>::~allocator();
  std::string::string(local_48);
  std::string::string(local_58);
  plVar1 = std::operator<<(&std::cout,"Please, login with your credentials.");
  std::ostream::operator<<(plVar1,std::endl<>);
  std::operator<<(&std::cout,"Username:");
  std::operator>>(&std::cin,local_48);
  uVar2 = std::operator==(local_48,local_28);
  if ((char)uVar2 == '\0') {
    std::operator<<(&std::cout,"GTFO you lame ass hacker.");
  }
  else {
    plVar1 = std::operator<<(&std::cout,"Now, please insert the password.");
    std::ostream::operator<<(plVar1,std::endl<>);
    std::operator<<(&std::cout,"Password:");
    std::operator>>(&std::cin,local_58);
    uVar2 = std::operator==(local_58,local_38);
    if ((char)uVar2 == '\0') {
      std::operator<<(&std::cout,"GTFO you lame ass hacker.");
    }
    else {
      std::operator<<(&std::cout,"You have successfully logged into the system.");
    }
    std::istream::ignore((istream *)&std::cin);
    std::istream::ignore((istream *)&std::cin);
  }
  std::string::~string(local_58);
  std::string::~string(local_48);
  std::string::~string(local_38);
  std::string::~string(local_28);
  return 0;
}

## Cracking

What I though when cracking this is that right after the username and password fields:

 std::operator<<(&std::cout,"Username:");
 std::operator<<(&std::cout,"Password:");

 It called on a variable that had been set up earlier in the function (local_28 and local_38):

std::string::string(local_28,"EXAMPLEUSERNAME");
std::string::string(local_38,"EXAMPLEPASSWORD");

Assuming these variables are the username (local_28) and password(local_38) I will enter them into the program, and the program outputs "You have successfully logged into the system.", which is the success message.