# Chapter 8
## Configuring authorization: Applying restrictions

## This chapter covers:
- Selecting requests to apply restrictions using matcher methods
- Learning best-case scenarios for each matcher method


## Sections
- 8.1 Using matcher methods to select endpoints
- 8.2 Selecting requests for authorization using MVC matchers
- 8.3 Selecting requests for authorization using Ant matchers
- 8.4 Selecting requests for authorization using regex matchers
- Summary

## Notes:
Common expressions used for path matching with MVC matchers
| Expression        | Description |
| ------------- |:-------------|
| /a     | Only path /a. |
| /a/*     | The * operator replaces one pathname. In this case, it matches /a/b or /a/c, but not /a/b/c.      |  
| /a/** | The ** operator replaces multiple pathnames. In this case, /a as well as /a/b and /a/b/c are a match for this expression.    |  
| /a/{param} |    This expression applies to the path /a with a given path parameter.   |
| /a/{param:regex} |    This expression applies to the path /a with a given path parameter only when the value of the parameter matches the given regular expression.   |

## Summary

- In real-world scenarios, you often apply different authorization rules for different requests.
- You specify the requests for which authorization rules are configured based on path and HTTP method. To do this, you use matcher methods, which come in three flavors: MVC, Ant, and regex.
- The MVC and Ant matchers are similar, and generally, you can choose one of these options to refer to requests for which you apply authorization restrictions.
- When requirements are too complex to be solved with Ant or MVC expressions, you can implement them with the more powerful regexes.