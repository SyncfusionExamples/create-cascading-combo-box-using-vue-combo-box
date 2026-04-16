# Cascading ComboBox Using Vue ComboBox

**Repository Description:** A Vue.js project demonstrating cascading ComboBox components using Syncfusion, where dependent ComboBoxes populate based on parent selections.

## Overview

Learn how to create a cascading ComboBox using Syncfusion Vue ComboBox. This project shows how to add multiple ComboBox components and populate dependent ComboBoxes based on parent selections—ideal for country-state scenarios and similar dependent dropdowns.

## Prerequisites

- Node.js (v12 or higher)
- Vue CLI (v4 or higher)
- npm (v6 or higher)

## Installation

Clone the repository:
```bash
git clone https://github.com/SyncfusionExamples/create-a-cascading-combo-box-using-vue-combo-box combobox-component
cd combobox-component
npm install
```

## Running the Application

Start the development server:
```bash
npm run serve
```

Navigate to `http://localhost:8080/`. The app reloads on file changes.

## How It Works

1. First ComboBox selection triggers an event
2. Selected value filters/fetches data for the second ComboBox
3. Second ComboBox updates its data source dynamically
4. Extend this pattern to multiple cascading levels

## Resources

- **Demo**: [Cascading ComboBox Example](https://ej2.syncfusion.com/vue/demos/#/material/combo-box/cascading.html)
- **Docs**: [Cascading Guide](https://ej2.syncfusion.com/vue/documentation/combo-box/how-to/cascading)
- **Vue CLI**: [Vue-Cli README](https://github.com/vuejs/vue-cli/blob/master/README.md)

## Support

For help, check the Syncfusion Vue ComboBox documentation and Vue.js resources.
