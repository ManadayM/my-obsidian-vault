---
template: course
progress: 0%
priority: 0
url: https://app.pluralsight.com/library/courses/angular-2-getting-started-update/table-of-contents
---
![tp.web.random_picture](https://images.unsplash.com/photo-1483666852720-824ca74c50ca?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY3NzM5MjU5Mg&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# [Angular Getting Started](https://app.pluralsight.com/library/courses/angular-2-getting-started-update/table-of-contents)

## Section 2: Introduction

### 2.1: Introduction
- Angular is a [[JavaScript]] framework to build small/large client-side applications.
- Expressive HTML.
- Powerful data binding.
- Modular design.
- Built-in integration for communication with a back-end server.

### 2.2: Anatomy of an Angular Application
- The basic building blocks of an Angular app are - Modules, Components, and Services.
- Components = Template (HTML => UI) + Class (Properties and Methods => Code) + Metadata (Extra data).
- The services provide functionality across components like data fetching, logging, and exception handling.

### 2.5: Course Outline
- Components
- Templates, Interpolation, and Directives.
- Data Binding & Pipes.
- Nested components
- Services and DI
- HTTP data fetching
- Navigation and routing
- Modules

## Section 4: Components

### Component
An Angular Component is a view defined in a template (HTML with bindings and directives), and its associated code is defined with the class, and metadata is defined with a decorator.

### Creating a new component
```typescript
import { Component } from '@angular/core';

@Component({
	selector: 'app-root',
	template: `
		<div>
			<h1>{{pageTitle}}</h1>
			<div>My first component</div>
		</div>
	`
})
export class AppComponent {
	pageTitle: string = 'Acme Product Management';
}
```

> [!INFO] Decorator
> A function that adds **metadata** to a class, its members, or its method arguments. Prefixed with an @ sign. Angular provides built-in decorators like `@Component()`.



## 📚 Linked Notes
```dataview
TABLE file.cday AS Created 
FROM [[Angular Getting Started]]
WHERE contains(template, "note") 
SORT file.cday ASC
```

---
#### Internal Links
[[Courses]]
