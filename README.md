# Getting Started with Syncfusion Vue 3 Scheduler

A comprehensive guide to integrating the Syncfusion Vue Scheduler component into Vue 3 applications. This project demonstrates essential setup steps including package installation, CSS imports, component registration, and event data binding for building powerful scheduling solutions.

## Installation

Install the Scheduler component from npm registry:

```bash
npm install @syncfusion/ej2-vue-schedule --save
```

## CSS Configuration

Add required Syncfusion CSS styles to your `src/App.vue` file:

```js
import '../node_modules/@syncfusion/ej2-base/styles/material.css';
import '../node_modules/@syncfusion/ej2-buttons/styles/material.css';
import '../node_modules/@syncfusion/ej2-calendars/styles/material.css';
import '../node_modules/@syncfusion/ej2-dropdowns/styles/material.css';
import '../node_modules/@syncfusion/ej2-inputs/styles/material.css';
import '../node_modules/@syncfusion/ej2-navigations/styles/material.css';
import '../node_modules/@syncfusion/ej2-popups/styles/material.css';
import '../node_modules/@syncfusion/ej2-vue-schedule/styles/material.css';
```

## Component Setup

Import and register the Scheduler component with its directives in your Vue component. The component supports multiple built-in views (Day, Week, WorkWeek, Month, Agenda) along with resource scheduling and drag-and-drop functionality.

## Quick Start Example

Here's a minimal example to get started:

```html
<template>
    <ejs-schedule height='550px' width='100%' :selectedDate='selectedDate' :eventSettings='eventSettings'>
        <e-views>
            <e-view option='Day'></e-view>
            <e-view option='Week'></e-view>
            <e-view option='Month'></e-view>
        </e-views>
    </ejs-schedule>
</template>

<script>
import { ScheduleComponent, Day, Week, Month } from "@syncfusion/ej2-vue-schedule";

export default {
    name: "App",
    components: {
        'ejs-schedule': ScheduleComponent
    },
    data() {
        return {
            selectedDate: new Date(2021, 7, 12),
            eventSettings: { dataSource: [] }
        };
    },
    provide: {
        schedule: [Day, Week, Month]
    }
};
</script>
```

## Running the Application

Launch your application with:

```bash
npm run serve
```

## Documentation

Learn more about Syncfusion Vue Scheduler:

- **Vue Introduction:** https://ej2.syncfusion.com/vue/documentation/introduction
- **Schedule Component:** https://ej2.syncfusion.com/vue/documentation/schedule/getting-started