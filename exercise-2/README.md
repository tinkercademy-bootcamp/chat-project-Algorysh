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
- Why was this link chosen instead?
  - This link was chosen because it was free and publicly available and it closely matches the final standard.
- Is this a helpful reference for learning C++?
  - It is very dense and written for advanced users so we can use this for understanding precise rules. For most learners, books and other resources are more approachable.
- Can the various implementations of C++ compilers be different from the
  C++ standard?
  - Yes, it can be different. While all major compilers aim to conform to the standard, there may be differences due to incomplete implementation of new features, compiler-specific extensions, additional features or bugs.
- Where is the equivalent spec for C++26?

- Where do you find the spec for the HTTP protocol?
- What about HTTPS? Is there a spec for that protocol?

## Introduction to C++ and Sockets Programming

- Read the code in `src/`
- Are there any bugs in this code? 
- What can you do to identify if there are bugs in the code?

## Refactoring: Extract Function

- What is different in this code compared to exercise-1?
- Is this code better or worse than exercise-1?
- What are the tradeoffs compared to exercise-1?
- Are you able to spot any mistakes or inconsistencies in the changes?
  
## Thinking About Performance

- Does writing code this way have any impact on performance?
- What do we mean when we say performance?
- How do we measure performance in a program?

## Play with Git

- There isn't necessarily a single correct answer for how to abstract the 
  code from exercise-1 into functions
- Try different ways to refactor the code from exercise-1 to make it more
  readable.
- Make sure to commit each change as small and self-contained commit
- This will make it easier to revert your code if you need to
- What is `git tag`? How is `git tag` different from `git branch`?
- How can you use `git tag` and `git branch` to make programming easier and
  more fun?

## Learn Basics of Debugging in Your IDE

- How do you enable debug mode in your IDE?
- In debug mode, how do you add a watch?
- In debug mode, how do you add a breakpoint?
- In debug mode, how do you step through code?

### Memory Management and Debug Mode in Your IDE

- How do you see the memory layout of a `std::string` from your IDE debug mode?
- How do you see the memory layout of a struct from your IDE debug mode?