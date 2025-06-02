# Coding Conventions

Coding conventions are drag to follow and quite frustrating too but they are what keeps the collaboration and large scale project glued together without making it a spaghetti.

So it will be a long one be prepared. If you want to jump to other section and come back to this one later you can do that too.

> [!NOTE]
>
> For some guides like `Open source contribution` we recommend you first go through your respective coding convention before moving onto them.

### Table of contents

1. [Common practices](#common-practices)
1. [Frontend Developers](#frontend-developers)
1. [Backend Developers](#backend-developers)
1. [App Developers](#app-developers)

### Common practices

In this section we will look through some common practices that needs to be followed by each and every type of developers.

**Rules**

1. Always use `lowerCamleCase` convention for **variables and functions** name unless enforced by the programming language itself.
2. For `constants` and `enums` though use `UPPER_SNAKE_CASE` convention.
3. For `classes` use `UpperCamelCase` convention unless enforced by the programming language itself.
4. Use the concept of `DRY (Donot Repeat Yourself)` only when you have to copy and paste the code more than **3 times** if less than 3 times you can just copy and paste the code.
5. Follow the **folder structure** as specified in each type of project.

### Frontend developers

In this section we will talk about rules and conventions that are specific to frontend developers.

> [!NOTE]
>
> For now we use only `React` /`Next JS` and `Vue` / `Nuxt` as the frontend library and framework of choices.

**Rules for React / Next Js**

1. Use `UpperCamelCase` convention for naming component functions.
2. Use `lowerCameCase` convention for functions other than component.
3. Folder structure to follow for `React` based projects

```
> src
    > components (for global components)
    > utils (for utility functions)
      > configs (configuration files)
      > hooks (custom hooks)
      > helpers (helper functions)
    > routes (for routes related codes)
    > theme (for theme configuration [if needed])
    > app
      > store (state management store)
      > features (state management features)
    > provider (provider components [if needed])
    > layout (for layout components)
    > pages (for pages inside the project)
      > public (public pages)
        > _components (for local components)
      > private (authentication protected pages)
        > _components (for local components)
```

> [!TIP]
>
> There is work going on in an open source project called `beej` for creating React and Vue based application with folder structure and configuration already scaffolded. You can use the library to start with new project.

### Backend developers

In this section we will go through the rules and conventions that are specific to backend developers.

> [!NOTE]
>
> For now we use only `Node JS` and `Go` as the backend scripting languages.

**Rules for Node Js**

1. Folder structure to follow for `Node` based projects. _Note: for express based self creating projects_

```
> src
    > utils (for utility functions)
      > configs (configuration files)
      > helpers (helper functions)
      > db (database related configuration files)

    <!-- For express self creating -->
    > routes (for api endpoints)
    > controllers (for controllers - connector for service function with api endpoints)
    > services (for services main function where actual business logic happens)
    <!--  -->

    - index.{js|ts}  (entry point of the server)
```

> [!TIP]
>
> When using other frameworks like `Nest JS` follow the folder convention of the framework first then add the **utils** folder for any utility functions.

### App developers

In this section we will look at the rules and conventions that are specific to mobile app developers.

> [!NOTE]
>
> For now we use only `Flutter` and `React Native` as the framework of choices.

**Rules for Flutter**

1. Folder structure to follow for `React` based projects

```
> src
    > widgets (for global widgets)
    > utils (for utility functions)
      > configs (configuration files)
      > helpers (helper functions)
    > routes (for routes related codes)
    > theme (for theme configuration)
    > app
      > (folder structure as per state management library choosen)
    > provider (provider codes)
    > layout (for layout screens)
    > screens (for screens inside the project)
      > public (public screens)
        > _widgets (for local widgets)
      > private (authentication protected screens)
        > _widgets (for local widgets)
```

> [!TIP]
>
> There is an effort going to create `a template repo` with **theme and folder structure** already created. You can use that to start a new repo.
