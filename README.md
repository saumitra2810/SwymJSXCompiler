# SwymJSXCompiler
Setup code that can be used to create and override Swym UI components

## Setup

You will need npm and Node.JS installed to setup this project. Clone this repository and run ```npm install```. This will install all dependencies on your machine. 

## Quickstart Guide

Here's how you can create a new component - 

**Step 1**
Add a new file in the jsx folder and write the JSX markup for it like so - 

```
function SwymNotification(props, getHandler){
  return (
    <img attrs={{ src: props.product.imageurl }} />
    <h2>{props.product.title}</h2>
  )    
}
```

**Step 2**
Run the command ```npm run jsx``` in the root directory of this project. This will create a folder called jsx-compiled with your file in it.


**Step 3**
Copy the contents of your file from the jsx-compiled folder and paste them in the Shopify theme editor inside a new file. 


**Step 4**
Use the following code to override the Swym default component with your custom component.
```
    SwymUiCore.registerComponent(componentName, componentFunction)
```

Here, the ```componentFunction``` will be the function you wrote and pasted in the Shopify theme editor. For eg., here it will be SwymNotification.
