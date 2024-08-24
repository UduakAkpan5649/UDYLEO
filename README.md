# UDYLEO
# My first deployment
# First deployment transaction ID
# at1pz2a0sgx4633kckc554zscyvnmq596f9dj0wtelgtxlnx5tuxypsruhqk4

# Details
# Using the leo raw main 3u32 2u32 comand i was able to create my main.aleo file in the playground
# ![image](https://github.com/user-attachments/assets/2db43bc8-eb3e-4554-a0b0-fb65c6dffd3b)

![image](https://github.com/user-attachments/assets/345bc47e-9c45-4833-af4b-1080788b1d90)


# Second Deployment
# Second deploy transaction ID
# at1fhzfy7gdc7mfydvwm4a62e767w62ztmjuj5qwg79szmnllrnrsyqute534

# Details
# Using Playground i run this command leo run main 3u32 2u32 to build a main.aleo file inside
# ![image](https://github.com/user-attachments/assets/46a448b9-d164-48ea-ac90-1f78d2f44391)


# First deployment command : 

program helloworld_udy.aleo;
function main:
    input r0 as u32.public;
    input r1 as u32.private;
    add r0 r1 into r2;
    output r2 as u32.private;

# Second deployment command
program simple_token_udy.aleo;

record Token:
    owner as address.private;
    amount as u64.private;

function mint:
    input r0 as address.private;
    input r1 as u64.private;
    cast r0 r1 into r2 as Token.record;
    output r2 as Token.record;

function transfer:
    input r0 as Token.record;
    input r1 as address.private;
    input r2 as u64.private;
    sub r0.amount r2 into r3;
    cast r0.owner r3 into r4 as Token.record;
    cast r1 r2 into r5 as Token.record;
    output r4 as Token.record;
    output r5 as Token.record;
