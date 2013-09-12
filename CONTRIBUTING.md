JBoss Archetypes Contributing Guide
===================================

Archetype is a Maven project templating toolkit

Basic Steps
-----------

To contribute to the Archetypes, fork the Archetypes repository to your own Git, clone your fork, commit your work on topic branches, and make pull requests. 

If you don't have the Git client (`git`), get it from: <http://git-scm.com/>

Here are the steps in detail:

1. [Fork](https://github.com/jboss-jdf/jboss-as-archetype/fork_select) the project. This creates a the project in your own Git.

2. Clone your fork. This creates a directory in your local file system.

        git clone git@github.com:<your-username>/jboss-as-archetype.git

3. Add the remote `upstream` repository.

        git remote add upstream git@github.com:jboss-jdf/jboss-as-archetype.git

4. Get the latest files from the `upstream` repository.

        git fetch upstream

5. Create a new topic branch to contain your features, changes, or fixes.

        git checkout -b <topic-branch-name> upstream/master

6. Contribute new code or make changes to existing files. Make sure that you follow the General Guidelines below.

7. Commit your changes to your local topic branch. You must use `git add filename` for every file you create or change.

        git add <changed-filename>
        git commit -m `Description of change...`

8. Push your local topic branch to your github forked repository. This will create a branch on your Git fork repository with the same name as your local topic branch name.

        git push origin HEAD            

9. Browse to the <topic-branch-name> branch on your forked Git repository and [open a Pull Request](http://help.github.com/send-pull-requests/). Give it a clear title and description.

General Guidelines
------------------

* We strongly encourage you to discuss your planned archetype on the [dev list](http://www.jboss.org/jdf/forums/jdf-dev/) before starting.

* The archetype should be formatted using the JBoss AS profiles found at <https://github.com/jboss/ide-configs/tree/master/ide-configs>

* More instructions, see the [Guide to Creating Archetypes](http://maven.apache.org/guides/mini/guide-creating-archetypes.html)

* If possible, create a cheat sheet for the archetype to guide users and developers through the example. See the [Archetype Cheat Sheet Contributing Guide](#archetype-cheat-sheet-contributing-guide) for more information.

License Information and Contributor Agreement
---------------------------------------------

  JBoss Developer Framework is licensed under the Apache License 2.0, as we believe it is one of the most permissive Open Source license. This allows developers to easily make use of the code samples in JBoss Developer Framework. 

  There is no need to sign a contributor agreement to contribute to JBoss Developer Framework. You just need to explicitly license any contribution under the AL 2.0. If you add any new files to JBoss Developer Framework, make sure to add the correct header.

### Java

      /*
       * JBoss, Home of Professional Open Source
       * Copyright <Year>, Red Hat, Inc. and/or its affiliates, and individual
       * contributors by the @authors tag. See the copyright.txt in the 
       * distribution for a full listing of individual contributors.
       *
       * Licensed under the Apache License, Version 2.0 (the "License");
       * you may not use this file except in compliance with the License.
       * You may obtain a copy of the License at
       * http://www.apache.org/licenses/LICENSE-2.0
       * Unless required by applicable law or agreed to in writing, software
       * distributed under the License is distributed on an "AS IS" BASIS,  
       * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
       * See the License for the specific language governing permissions and
       * limitations under the License.
       */

### XML

      <!--
       JBoss, Home of Professional Open Source
       Copyright <Year>, Red Hat, Inc. and/or its affiliates, and individual
       contributors by the @authors tag. See the copyright.txt in the 
       distribution for a full listing of individual contributors.

       Licensed under the Apache License, Version 2.0 (the "License");
       you may not use this file except in compliance with the License.
       You may obtain a copy of the License at
       http://www.apache.org/licenses/LICENSE-2.0
       Unless required by applicable law or agreed to in writing, software
       distributed under the License is distributed on an "AS IS" BASIS,  
       WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
       See the License for the specific language governing permissions and
       limitations under the License.
       -->

### Properties files

       # JBoss, Home of Professional Open Source
       # Copyright 2012, Red Hat, Inc. and/or its affiliates, and individual
       # contributors by the @authors tag. See the copyright.txt in the 
       # distribution for a full listing of individual contributors.
       #
       # Licensed under the Apache License, Version 2.0 (the "License");
       # you may not use this file except in compliance with the License.
       # You may obtain a copy of the License at
       # http://www.apache.org/licenses/LICENSE-2.0
       # Unless required by applicable law or agreed to in writing, software
       # distributed under the License is distributed on an "AS IS" BASIS,  
       # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
       # See the License for the specific language governing permissions and
       # limitations under the License.

Archetype Cheat Sheet Contributing Guide
==============================


Purpose of the Cheat Sheets
--------------------------

- Cheat sheets function as a tutorial and provide a step by step guide through a archetype. 
- They provide a way to step through and explain the code in an interactive way.
- They can provide an in-depth analysis of specific sections of code.


Basic Steps to Create a Cheat Sheet
-----------

You can create a cheat sheet using the Eclipse Wizard or you can copy and modify an existing cheat sheet from another archetype. This section describes how to create a cheat sheet using the Eclipse wizard.

_Note: Be sure your project folder is located outside of the Eclipse workspace before you begin this process._

1.  Import your archetype into JBoss Developer Studio (JDBS) .
    1.  From the menu, choose `File` --> `Import` --> `Maven` --> `Existing Maven Projects`, then click `Next`.
    2.  Navigate to your archetype, select it, then click `OK`.
    3.  Click `Finish`.
2.  Create the cheat sheet.
    1.  From the menu, choose `File` --> `New` --> `Other` --> `User Assistance` --> `Cheat Sheet`, then click `Next`.
    2.  Select the archetype folder, give it a name 'cheatsheet.xml', and choose `Simple Cheat Sheet`.
    3. Click `Finish`.
3.  Populate the cheatsheet with useful information to help a user understand the archetype.
    1.  Modify the title, for example: `helloworld archetype`
    2.  Add an introduction, for example: `This archetype demonstrates the use of CDI 1.0 and Servlet 3.0. It is a simple application that can be used to verify the JBoss EAP server is configured and running correctly.`
    3.  Add an `item` for each file or class you want to describe. 
        *  This is dependent on the archetype features you plan to demonstrate.
        *  Provide a good description.
        *  Add subitems to describe code sections and provide the line numbers that are referenced.
5. Test your cheat sheet by opening it in JDBS.
    1.  Go through each step and make sure the descriptions are valid.
    2.  Click on each link to make sure it opens the file and highlights the correct lines of code.
4. When you finish testing the cheat sheet, rename the file from `cheatsheet.xml` to `.cheatsheet.xml` and make sure it is located in the root directory of the archetype.


General Guidelines
------------------

* If your project folder is located in the Eclipse workspace when you generate your cheat sheet using the Eclipse wizard, it will generate an invalid project name and attempts to open source code will fail. Be sure your project folder is located outside the Eclipse workspace before you begin.
* The cheat sheet should be created in the root of the archetype directory and named `.cheatsheet.xml`. Eclipse will not let you name the file with a leading '.', so you will need to rename it after it is created.
* Use the replaceable value `${currentProject}` to avoid hard-coding the project path. This ensures that if the archetype folder is moved, the cheat sheet will work as expected.
* Do not use the `<action>` tag if it can be avoided. It is more fragile than the `<command>` tag, which uses parameters names instead of indexes.
* Try to highlight the most important features and code for the archetype. Pay particular attention to areas that might confuse developers. Cheat sheets require that users execute or skip each step, so you don't want to bore developers with the code that has no impact on the purpose of the archetype.

Find Help
------------------

You can find additional help at the following locations:

* [Eclipse Help: Cheat sheets](http://help.eclipse.org/kepler/index.jsp?topic=%2Forg.eclipse.platform.doc.isv%2Fguide%2Fua_cheatsheet.htm&resultof=%22cheat%22%20%22sheet%22%20)
* [Recommended Work Flow for Cheat Sheet Development](http://www.eclipse.org/pde/pde-ui/articles/cheat_sheet_dev_workflow/)
* [Max's cheat sheet example](https://github.com/maxandersen/cheatsheet-helloworld)


