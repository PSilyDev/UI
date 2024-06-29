- ## Change text color of placeholder in select tag
  We know that select does not have placeholder, so to create a placeholder, create an option -

  ```
  <option value="" disabled selected>Placeholder</option>
  ```
  - **selected** to keep it on the top on rendering
  - **disabled** so that it can't be selected

  Next,
  - Use the **:invalid pseudo-class:** This will target the select element when the placeholder option is selected.
  - Add a **required** attribute: This makes the default option invalid, which triggers the :invalid styles.
  - Set the **default** option's value to an empty string.

  The whole code looks like -
  ```
  <select
    className="invalid:text-slate-400 valid:text-black"
    defaultValue=""
    required>
      <option value="" disabled selected>Placeholder</option>
      <option value="high">Option 1</option>
  </select>
  ```
