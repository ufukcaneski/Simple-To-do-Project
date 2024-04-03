
# Simple To-do Project

## About me
[Linkedin](https://www.linkedin.com/in/UfukcanEski)
[Twitter](https://twitter.com/UfukcanEski)

## Project Description
This project shows how to create a simple to-do checklist app.

## Smart Contract Address
5AnwcrztGq7qezEHMCTFzSLH5WxbvBgPPRxDXWrM2oZD

## Installation Prerequisites

If you want to create a project on your local device; this requires installation of the following:

-  Install [IC SDK](https://internetcomputer.org/docs/current/developer-docs/setup/install/index.mdx).
    

Start by opening a terminal window.

**Step 1:** Navigate to the folder containing the project files and start a local instance of the copy with this command:

```
cd examples/motoko/simple-to-do
dfx start --background
```

**Step 2:**Deploy Canister:

```
dfx deploy
```

**Step 3:** Create a to-do checklist with the addTodo method:

```
dfx canister call simple_to_do addTodo '("Create a project")'
dfx canister call simple_to_do addTodo '("Build the project")'
dfx canister call simple_to_do addTodo '("Deploy the project")'
```

**Step 4:** Display the to-do checklist with the showTodos method:

```
dfx canister call simple_to_do showTodos
```

**Step 5:** Verify that the output returns the values you entered:

```
("
___TO-DOs___
(1) Create a project
(2) Build the project
(3) Deploy the project")
```

**Step 6:** Complete the to-do checklist item with the CompleteTodo method:

```
dfx canister call simple_to_do completeTodo '(1)'
```

**Step 7:** Display the to-do checklist with the showTodos method.
```
dfx canister call simple_to_do showTodos
```

**Step 8:** Verify that the return value matches the value you expect.

```
("
___TO-DOs___
(1) Create a project ✔
(2) Build the project
(3) Deploy the project")
```
