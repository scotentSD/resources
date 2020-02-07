
# Jekyll for Github Pages

**Jekyll** is a static site generator that's perfect for GitHub hosted blogs ([Jekyll Repository](https://github.com/jekyll/jekyll))
**Jekyll Now** makes it easier to create your Jekyll blog, by eliminating a lot of the up front setup.

- You don't need to touch the command line
- You don't need to install/configure ruby, rvm/rbenv, ruby gems :relaxed:
- You don't need to install runtime dependencies like markdown processors, Pygments, etc
- If you're on Windows, this will make setting up Jekyll a lot easier
- It's easy to try out, you can just delete your forked repository if you don't like it

- [Read more about Jekyll](jekyll)
- [Read this excellent Jekyll Cheatsheet when you are ready](https://devhints.io/jekyll)

# Markdown
**Markdown** is a super simple way of creating structured content
You edit a Markdown file such as **readme.md** using teh following syntax:

- **```#```**   symbol for top level heading.
- **```##```**   for second level heading.
- **```###```**   for tertiary heading.
- **```-```**   symbol for a list item.
- **```[name of link](url of link)```** to create links.
- Put files in a **```/files```** folder off of the root of each repository.
- Reference them with links like: **```[personas](/files/personas.pdf)```**.
- When you update anything you will have to **Commit** it to the **Repository**.
- At the bottom of whatever you are editing you will see a **Commit Changes** section. Use this to **Commit Changes**. This will be greyed out until any changes are made.




[Basic Markdown Primer](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


<br>
<div>Last updated: {{site.time | date_to_string}}</div>
