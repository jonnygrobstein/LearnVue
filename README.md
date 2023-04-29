# LearnVue

## What did I learn today?  

Vue.js

## Why did I want to learn it?
vue.js is what a company I'm going to be working with is using so I wanted to get acquainted with it prior to starting.

## What did you do to try to learn?  What process did you follow?
I started with a more academic training video series but that was a bit slow and over detailed.  Then I switched to a tutorial of building an app and was working through that and learning how the different parts of Vue work together.


### Notes from step by step training

Look into Vue CLI install approach.  Using npm for this project.

Vue version 5.0.8

#### Setting up a Vue.js project
1. npm install vue@next
2. npm install -g @vue/cli
3. check version vue --version
4. vue create <file name>
5. cd <file name>
6. npm run serve

App will be running locally on localhost:8080
To optimize/create a production build #6 is npm run build


#### .vue files have 3 sections
1. <template></template> - HTML
2. <script></script> - JS
3. <style></style> - CSS
Each page is self containing

**Components** = .vue file
.vue is a single vile component

connecting data present in the script block to the HTML present in the template block
Declrative programming approach

**Binding data** uses {{ double curly brackets with property name }}
or use a directive

`
<div v-text='channel'></div>
`

v-text is rarely used and slower and more restrictive

v-html can be used to utilize text css such as bold

*Be cautious of what you are rendering (api's can inject malicious code easily this way)*

### Break from academic training

App is a restaurant management app
Currently have the logins installed
Also used a local JSON Database for simplicity
