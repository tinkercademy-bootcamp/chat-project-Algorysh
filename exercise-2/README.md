# Exercise 2

**Update this README with your answers to the questions below.**

## Sources of Information for Questions from Before

### Socket 
- https://man7.org/linux/man-pages/man2/socket.2.html - System call reference
  for creating communication endpoints
- Or type `man socket` in terminal
- https://man7.org/linux/man-pages/man7/socket.7.html - Socket interface 
  overview and protocol families
- Or type `man 7 socket` in terminal
- When would you want to use a `SOCK_RAW` stream?
  We’d use a `SOCK_RAW` socket when we need low-level control over network communication. For example, if we want to build a tool like ping (which uses ICMP), a packet sniffer like tcpdump, or testing a custom protocol, raw sockets let us directly access and construct the packets ourselves. It’s powerful, but risky, so it's mostly used for things like diagnostics, monitoring, or security tools, and usually only by users with root access.

### TCP and IP Protocols
- [IPv4](https://www.rfc-editor.org/info/rfc791) - Internet Protocol 
  specification defining packet structure and routing
- [IPv6](https://www.rfc-editor.org/info/rfc8200) - Next-generation Internet 
  Protocol with expanded address space
- [TCP](https://datatracker.ietf.org/doc/html/rfc9293) - Transmission Control 
  Protocol providing reliable, ordered data delivery
    
### C++
- [C++23 ISO standard draft](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2023/n4950.pdf) - 
  Working draft of the C++ language specification
- Is the above the official C++23 spec? 
  - No, it's not the official C++23 spec, the final, officially ratified C++23 standard is ISO/IEC 14882:2024. The standardization process involves multiple working drafts and these drafts are used to refine the language and library features before the final standard is published.
- Where is the official C++23 spec?
  - The official C++23 spec is published as ISO/IEC 14882:2024 by ISO, and it's at [ISO website](https://www.iso.org/standard/79358.html).
  - This link was chosen because it was free and publicly available and it closely matches the final standard.
- Is this a helpful reference for learning C++?
  - It is very dense and written for advanced users so we can use this for understanding precise rules. For most learners, books and other resources are more approachable.
- Can the various implementations of C++ compilers be different from the
  C++ standard?
  - Yes, it can be different. While all major compilers aim to conform to the standard, there may be differences due to incomplete implementation of new features, compiler-specific extensions, additional features or bugs.
- What are the most widely used and most significant C++ compilers?
  The most widely used and significant C++ compilers are:
  - **GCC (GNU Compiler Collection):**
  - **Clang/LLVM:**
  - **MSVC (Microsoft Visual C++):**
  - **Intel C++ Compiler (ICC/ICX):**
- Where is the equivalent spec for C++26?
  - It's still under development. The latest working drafts and proposals are on the [ISO C++ committee papers page](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/).
- Where do you find the spec for the HTTP protocol?
  - The official HTTP specifications (like HTTP/1.1, HTTP/2, and HTTP/3) are on the IETF’s website as RFC documents — for example, [RFC 9112](https://datatracker.ietf.org/doc/html/rfc9112) for HTTP/1.1.
- What about HTTPS? Is there a spec for that protocol?
  - HTTPS is just HTTP layered over TLS. So, we have to look at both the HTTP RFCs and the [TLS spec](https://datatracker.ietf.org/doc/html/rfc8446), such as RFC 8446 for TLS 1.3.

## Introduction to C++ and Sockets Programming

- Read the code in `src/`
- Are there any bugs in this code? 
  - Nobugs are found after reviewing and testing.
- What can you do to identify if there are bugs in the code?
  - We can run the code and see if any error shows, if not then try running it with test cases and compare with expected output. Also try to read through the code to see if there is any bug.
  - To see what the bug is, we can use tools like gdb, lldb (for LLVM/Clang), valgrind.

## Refactoring: Extract Function

- What is different in this code compared to exercise-1?
  - In this code, we are using helper functions, instead of having all the logic in `main` which makes the code modular and easier to read.
- Is this code better or worse than exercise-1?
  - This code is better than exercise-1 as this is modular and easier to read and it's a good practice to use functions rather than writing all the logic in `main`.
- What are the tradeoffs compared to exercise-1?
  - In exercise-2, the code gets longer and there is an increased complexity due to multiple function calls (but this is negligible). It may be harder for a newbie to keep track of the code due to a lot of jumping through functions.
- Are you able to spot any mistakes or inconsistencies in the changes?
  - The error messages can be more descriptive as to why that error occurred.

## Thinking About Performance

- Does writing code this way have any impact on performance?
  - It can have a minor impact on the performance due to multiple function calls.
- What do we mean when we say performance?
  - Performance refers to how fast the code runs and how much memory it's using.
- How do we measure performance in a program?
  - Performance is measured through time and space complexities. We can use commands like `time` and `top` to measure these.

## Play with Git

- There isn't necessarily a single correct answer for how to abstract the 
  code from exercise-1 into functions
- Try different ways to refactor the code from exercise-1 to make it more
  readable.
- Make sure to commit each change as small and self-contained commit
- This will make it easier to revert your code if you need to
- What is `git tag`? How is `git tag` different from `git branch`?
  - `git tag` is used to mark an important event, usually a release, which we might want to refer to later. `git tag` marks a specific point in history while `git branch` creates a movable line of development.
- How can you use `git tag` and `git branch` to make programming easier and
  more fun?
  - we can use `git branch` to try things out and experiment with it, or we can use `git tag` to mark the known-good code and then try things out.

## Learn Basics of Debugging in Your IDE

- How do you enable debug mode in your IDE?
  - Press F5 to enable debug mode.
- In debug mode, how do you add a watch?
  - In watch panel, add the variable you want to watch.
- In debug mode, how do you add a breakpoint?
  - Click on the left of the line you want to add breakpoint on.
- In debug mode, how do you step through code?
  - Use buttons like Step Over (F10), Step Into (F11), and Step Out (Shift+F11) to move through your code line by line.

### Memory Management and Debug Mode in Your IDE

- How do you see the memory layout of a `std::string` from your IDE debug mode?
- How do you see the memory layout of a struct from your IDE debug mode?