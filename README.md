# How to - from idea to tasks
## 1. Request prompt - high level app idea

Start to iterate with the model to come up with the request to feed into other prompts, this is turn based and will take a couple of messages forth and back with the model to refine the details. 

Use a decent reasoning model (o3, Gemini 2.5 Pro) that can do web-search. 


## 2. Spec prompt - get detailed PRD

Uses output from previous Request Prompt iteration `<project_request>` to generate the full PRD incl. technical specification.

Add rules about project/technical architecture in `<project_rules>`

Add existing boilerplate project code in `<starter_template>` - use tools like Gitingest, Repoprompt, Repomix

Once you're happy you will have your final PRD/Tech Spec.


## 3. Move PRD to Cursor and do task-breakdown

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
