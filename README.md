## How to 
### Request Prompt 

Start to iterate with the model to come up with the request to feed into other prompts, this is turn based and will take a couple of messages forth and back with the model to refine the details. 

Use a decent reasoning model (o3, Gemini 2.5 Pro) that can do web-search. 


### Spec Prompt 

Uses output from previous Request Prompt iteration <project_request> to generate the full PRD incl. technical specification.

Add rules about project/technical architecture in <project_rules>

Add existing boilerplate project code in <starter_template> - use tools like Gitingest, Repoprompt, Repomix

Once you're happy you will have your final PRD/Tech Spec.

### Move PRD to Cursor and do task-breakdown

Take the PRD and place it into your project as `prd.md`

Then initialize task-master and run following commands: 
```
tm parse-prd
```

```
tm generate
```

```
tm analyze-complexity
```

```
tm complexity-report
```

```
tm expand --all 
```
