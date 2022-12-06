List of commands:- 

1) npx create-nx-workspace 
        // Create a new nx workspace 
                --> Choose integrated style --> choose apps (Our workspace will be empty without application)

2) npm install -D @nrwl/angular 
        //install angular in our nx workspace

3) nx generate @nrwl/angular:app project-1 
        // generate an angular application with the name project-1

4) nx generate @nrwl/angular:app project-2 
        //generate an angular application with the name project-2

5) nx generate @nrwl/angular:lib shared 
        //generates a library inside the /libs folder named shared

6)cd libs/shared/src/lib 
        // stepping into the shared library directory

7)nx generate @nrwl/angular:component header 
        //generate a component inside the library we created
                 --> write the html, css and functions needed in this component. You can use tailwind or any other 
                     frameworks you want.

9)  exports: [HeaderComponent] 
        // mention your component in the exports of the shared.module.ts file so that it 
        can be imported by the projects 

10) export * from './lib/header/header.component' 
        //export your component from your index.ts file as well

11) import { SharedModule } from '@nx/shared'; 
        //go to your project's app.module.ts file and import the shared module
                imports: [BrowserModule, SharedModule],
                -->also mention SharedModule in the imports section of the app.module.ts file

12) import { HeaderComponent } from '@nx/shared'; 
        //after importing the library module in your app module, go to the app.component.ts file and import your header component as well

13) <nx-header></nx-header> 
        //go to your html file and use the selector of your shared component to have a view in the html  

