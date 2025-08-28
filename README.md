# How to - from idea to tasks


## 1. Request prompt - high level app idea ⚡

[Copy the prompt](https://github.com/gibgutzi/idea-studio/blob/373f6d2020f93a080a4a041700e8e85f4bc1b672/request-prompt.md) and paste it into the chat interface of your choice. Use a decent reasoning model (o3, Gemini 2.5 Pro) that can do web-search. Start to iterate with the model to come up with the request to feed into other prompts, this is turn based and will take a couple of messages forth and back with the model to refine the details. 


## 2. Spec prompt - get detailed PRD 📝

[Copy the prompt](https://github.com/gibgutzi/idea-studio/blob/373f6d2020f93a080a4a041700e8e85f4bc1b672/spec-prompt.md) to use in chat interface of your choice.

Uses output from previous Request Prompt iteration `<project_request>` to generate the full PRD incl. technical specification.

Add rules about project/technical architecture in `<project_rules>`

Add existing boilerplate project code in `<starter_template>` - use tools like Gitingest, Repoprompt, Repomix for this, beware of context window limits 

Once you're happy you will have your final PRD/Tech Spec.


## 3. Move PRD to Cursor and do task-breakdown 📋

Take the PRD and place it into your project as `prd.md`

Then initialize [Taskmaster AI](https://www.task-master.dev/) and run following commands: 


Generate tasks from a PRD document:
```  
tm parse-prd --input=<prd-file>
```

Create individual task files from tasks.json:
```
tm generate
```

Analyze tasks and generate expansion recommendations:
```
tm analyze-complexity
```

Display the complexity analysis report:
```
tm complexity-report
```

Expand all pending tasks with subtasks:
```
tm expand --all 
```

## 4. Set up Cursor Rules 📜

Set user rules if you want in Cursor Settings > Rules & Memories > User Rules 
- [User rules by Shaoru from Cursor](https://github.com/gibgutzi/idea-studio/blob/edf3063f09c03d8bca7ad22d515928d9efebaf51/cursor-user-rules.md)

Set up additional rules for your project 
- Run /Generate Cursor Rules in Cursor's AI Pane 
