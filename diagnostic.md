# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    Something that has elements nested within it, like a navbar with buttons or input fields.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    Templates (template.hbs) and components (components.js).  Components define the actions and behavior of templates using JS and populate the model via the model hook.  Templates contain the HTMLbars content that will be displayed for that particular section.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{ each contact as |contact| }}
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{ each contact.phone as |phone| }}
      {{my-phone phone=phone}}
    {{/each}}
    ```
