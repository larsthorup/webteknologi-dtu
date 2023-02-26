# Forms - front-end web technology - 2023-03-06

Enable users to enter information.

Please read:

- [Your first form](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form)
- [How to structure a web form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form)
- [Basic native form controls](https://developer.mozilla.org/en-US/docs/Learn/Forms/Basic_native_form_controls)
- [The HTML5 input types](https://developer.mozilla.org/en-US/docs/Learn/Forms/HTML5_input_types)
- [Other form controls](https://developer.mozilla.org/en-US/docs/Learn/Forms/Other_form_controls)(
- [Client-side form validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
- [Reacting to input with state](https://beta.reactjs.org/learn/reacting-to-input-with-state)
- [Sharing State Between Components](https://beta.reactjs.org/learn/sharing-state-between-components)
- [React `<input>`](https://beta.reactjs.org/reference/react-dom/components/input)

## Why are forms exciting?

- Forms - _all_ apps need users to enter information
- Forms are a high agony necessity - lots of UX opportunities

## Forms

- Form element: onSubmit
- Submit button
- Form controls: input, select, textarea
- Label
- Input controls for typing: text, number, email, password
- Input controls for toggling: checkbox, radio
- Select control
- Textarea control
- File upload input
- Autofocus
- Special controls: range, date, time, color, datalist, progress, meter

## Form validation

- All client-side validation must always be **in addition to** server-side validation
- **Prevent** invalid input (e.g. numeric input)
- **Immediate feedback**, if not too "loud" (e.g. new passwod input)
- **Feedback on submit**, otherwise
- Required fields, valid range, valid format
- Cross field validation (new password)
- Style depending on input being valid
- Custom validation error reporting (message, layout)

## React controlled vs untrolled components

- Controlled components: no state, controlled from outside with props
- Uncontrolled components: internal state, not fully controllable from outside
- Examples:
  - Controlled components:
    - Accordion / Tabs sections
    - `<input value={currentValue}>`
  - Uncontrolled components:
    - Expandable / collapsible section
    - `<input type="file">`
    - `<input defaultValue={initialValue}>`
- Controlled pros / cons:
  - more fine-grained customization, such as character limitations, disable submit when invalid
  - more effort to work well, risk of "jumbled" input
- Uncontrolled pros / cons:
  - simpler, features like validation for free
  - less customizable, like validation error reporting

## Testing forms

- Use `.type()`, `.selectOption()`, `.click()` from `@testing-library/user-event`
- To replace value in `<input type="number">`, which cannot be blanked use this trick:
  - `user.type(numericInput, "5{arrowleft}{backspace}")`
- Submit form by clicking the submit button
- Test validation using `.toBeValid()` and `.toBeInvalid()` from `jest-dom`.
- Test custom validation error message with `expect(input.validationMessage).toEqual("...")`

## Next time

[UX, styling](..).
