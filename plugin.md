<div id='toc'>
  <ul align='center'>
    <summary>
      <h1>🎯 Mod Lumina Template</h1>
    </summary>
  </ul>
</div>

<img
  role='presentation'
  src='https://raw.githubusercontent.com/Richard-Passos/readme-kit/9b17b6fa2fb567f76880adbfff92670166776c99/assets/dividers/cyber_bottom.svg'
/>

<br>
<br>

<div id='toc'>
  <ul>
    <summary>
      <h2>👀 Overview</h2>
    </summary>
  </ul>
</div>

<p>
  Lumina Template is a Moodle activity plugin that allows course authors to build visually rich course content using reusable templates. Instead of creating a different activity for every layout, the plugin provides a single activity where the author selects a template and configures only the content required by that template.
  
  Each template defines its own schema and layout. When a template is selected, the activity form is generated dynamically based on its schema, presenting only the settings relevant to that template.
  
  This allows different templates to offer tailored authoring experiences while sharing the same underlying plugin. As a result, new templates can be developed independently without requiring changes to the existing ones.
</p>

<h3>
  How it works:
</h3>

```text
Author adds a Lumina Template activity
├── Selects a template
├── Plugin generates the form
├── Author fills in the content
├── Plugin validates and stores the data
└── Mustache renders the final HTML
```

<img
  role='presentation'
  src='https://raw.githubusercontent.com/Richard-Passos/readme-kit/9b17b6fa2fb567f76880adbfff92670166776c99/assets/dividers/cyber_badge.svg'
/>

<div id='toc'>
  <ul>
    <summary>
      <h2>🎬 Demo</h2>
    </summary>
  </ul>
</div>

<p>
  The following comparison illustrates the motivation behind Lumina Template. Before the plugin, course content was typically presented as a simple list of resources. With Lumina Template, the same content can be organized into reusable, visually rich layouts that provide a more engaging learning experience.
</p>

<h3>
  Before:
</h3>

<img
  src='https://raw.githubusercontent.com/napeadsead/mod_luminatemplate/refs/heads/master/before.gif?token=GHSAT0AAAAAAEAE52Z33WNPQLLOMFVP47RM2TLPRDA'
  alt="Before: a Lumina course displaying content as a simple list of links and resources."
/>

<h3>
  After:
</h3>

<img
  src='https://raw.githubusercontent.com/napeadsead/mod_luminatemplate/refs/heads/master/after.gif?token=GHSAT0AAAAAAEAE52Z24SNUE3ZUQ55VTY5E2TLPSCA'
  alt="After: the same course using Lumina Template to present content with rich, structured layouts."  
/>

<img
  role='presentation'
  src='https://raw.githubusercontent.com/Richard-Passos/readme-kit/9b17b6fa2fb567f76880adbfff92670166776c99/assets/dividers/cyber_badge.svg'
/>

<div id='toc'>
  <ul>
    <summary>
      <h2>✨ Features</h2>
    </summary>
  </ul>
</div>

<ul>
  <li>
    <b>Modern Course Experience</b>: Provides visually rich and responsive layouts that enhance the presentation of course content.
  </li>

  <li>
    <b>Reusable Templates</b>: Choose from multiple pre-defined templates, each with its own schema and layout.
  </li>

  <li>
    <b>Internationalization</b>: Every template supports multiple languages through Moodle's language system, allowing content to be presented according to the user's selected language.
  </li>

  <li>
    <b>Dynamic Forms</b>: Each template generates its own form dynamically, displaying only the fields required for that template.
  </li>
  
  <li>
    <b>Integrated Documentation</b>: Every template includes built-in documentation with summary and a live preview.
  </li>

  <li>
    <b>Extensible Architecture</b>: New templates can be added independently, without modifying existing ones.
  </li>
</ul>

<img
  role='presentation'
  src='https://raw.githubusercontent.com/Richard-Passos/readme-kit/9b17b6fa2fb567f76880adbfff92670166776c99/assets/dividers/cyber_badge.svg'
/>

<div id='toc'>
  <ul>
    <summary>
      <h2>💬 FAQ</h2>
    </summary>
  </ul>
</div>

<details>
  <summary><b>What is this plugin?</b></summary>
  
  Lumina Template is a Moodle activity plugin that allows course authors to create visually rich course content without writing HTML or requiring a different activity for every layout.
  
  Instead of implementing multiple activities for different designs, the plugin provides a single extensible activity where the author simply selects a template and fills in its content. Each template defines its own schema and layout, allowing new designs to be added independently without modifying the plugin core.
  
  This approach simplifies maintenance, keeps the authoring experience consistent, and makes the plugin easy to extend over time.
</details>

<details>
  <summary><b>What is an activity?</b></summary>
  
  In Moodle, an <b>activity</b> is a type of course resource that users can interact with, such as an Assignment, Quiz, Forum, or Page. Authors add activities to a course to provide content or collect student interactions.
  
  Lumina Template is one of these activities. When an author adds it to a course, they can choose one of the available templates, configure its content through a dynamic form, and the plugin renders the final layout.
</details>

<details>
  <summary><b>What is a template?</b></summary>
  
  A template is a self-contained component that defines a specific content. It includes everything needed to configure and display that template, such as its schema, layout (Mustache), and documentation.
  
  Each template is independent from the others, allowing new layouts to be added, modified, or removed without affecting the rest of the plugin.
</details>

<details>
  <summary><b>What is a schema?</b></summary>
  
  A schema is the central definition of a template. It describes which fields the template contains and how they should behave.
  
  The plugin uses the schema throughout the template's lifecycle to generate the activity form, validate user input, store the submitted data in the database, and provide a structured dataset for rendering the final content.
</details>

<details>
  <summary><b>What is Mustache?</b></summary>
  
  Mustache is the templating engine used by Moodle to generate HTML. In this plugin, each template includes its own Mustache file that defines how the configured content is displayed.
  
  Think of it as the view layer: it receives data (structure by the schema) from the renderer and is responsible only for presenting it.
</details>

<details>
  <summary><b>Why templates instead of HTML?</b></summary>
  
  Templates provide a consistent authoring experience, validate user input automatically, support multilingual content, and allow layouts to evolve without requiring authors to edit HTML.
</details>

<details>
  <summary><b>How do I add a new template?</b></summary>
  
  Create a new template following the project structure, implement its schema and layout (via Mustache) in the plugin templates folder, and add the required language strings and assets for documentation.
  
  For a complete step-by-step guide, see <a href='./docs/templates.md'>Templates</a>.
</details>

<details>
  <summary><b>How do I modify an existing template?</b></summary>
  
  Each template is isolated from the others. Update the template's schema, layout (Mustache), strings or assets as needed without affecting unrelated templates.
  
  Refer to <a href='./docs/templates.md'>Templates</a> for the recommended workflow.
</details>

<img
  role='presentation'
  src='https://raw.githubusercontent.com/Richard-Passos/readme-kit/9b17b6fa2fb567f76880adbfff92670166776c99/assets/dividers/cyber_badge.svg'
/>

<div id='toc'>
  <ul>
    <summary>
      <h2>📋 Requirements</h2>
    </summary>
  </ul>
</div>

<ul>
  <li>
    <a href='https://download.moodle.org/windows'><b>Moodle 4.5⁺</b></a>
  </li>
  
  <li>
    <b>PHP 8.3⁺</b> (provided by Moodle)
  </li>
  
  <li>
    <b>Bootstrap 4.6⁺</b> (provided by Moodle)
  </li>
  
  <li>
    <a href='https://github.com/napeadsead/theme_lumina_front'><b>Moove Theme 4.7⁺</b> (Lumina version)</a>
  </li>
</ul>

<br>

> [!NOTE]
> This plugin is designed to work exclusively with <b>Moove Theme 4.7⁺ (Lumina version)</b>. Other Moodle themes are not officially supported and may not render templates correctly.

<img
  role='presentation'
  src='https://raw.githubusercontent.com/Richard-Passos/readme-kit/9b17b6fa2fb567f76880adbfff92670166776c99/assets/dividers/cyber_badge.svg'
/>

<div id="toc">
  <ul>
    <summary>
      <h2>📚 Documentation Guide</h2>
    </summary>
  </ul>
</div>

<p>
  The documentation is organized by topic. If you're new to the project, start with Getting Started and continue with Architecture before creating or modifying templates.
</p>

<table>
  <thead>
    <tr>
      <th>Read</th>
      <th>What for?</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td><a href='./docs/getting-started.md'><b>Getting Started</b></a></td>
      <td>
        Set up the plugin and prepare your local development environment.
      </td>
    </tr>
    <tr>
      <td><a href='./docs/architecture.md'><b>Architecture</b></a></td>
      <td>
        Understand the project's structure, core files, and how its components work together.
      </td>
    </tr>
    <tr>
      <td><a href='./docs/templates.md'><b>Templates</b></a></td>
      <td>
        Learn how to create, read, update, and delete templates following the project's conventions.
      </td>
    </tr>
    <tr>
      <td><a href='./docs/fields.md'><b>Fields</b></a></td>
      <td>
        Explore how fields generate forms, validate input, and render template content.
      </td>
    </tr>
  </tbody>
</table>

<br>

> [!IMPORTANT]
> This documentation is intended for developers maintaining or extending the Lumina Template plugin.
