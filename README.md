# Accessible responsive form

In this example, we'll create a form that a customer can use to update their delivery and billing addresses.

Keep a browser window open alongside your code as you go.

## Part 1: Form structure

1. Create a `form` element. Give it an `action` attribute with a value of `#`.

2. Create an `input` element. Give it a `type` attribute with the value `submit`, and a `value` attribute with the value `Update addresses`. This element should stay at the end of the form.

## Part 2: Delivery address

### Text inputs

1. Create an `input` element. Give it the following attributes:
    - `type` attribute with the value `text`
    - `id` attribute with the value `first` (`id` will be used by the `for` attribute of the `label` element in the next step)
    - `name` attribute with the value `first` (`name` will be used by the form-handling script to grab the data from this field)
    - `placeholder` attribute with the value `Kenny`

2. Create a label element and wrap it around the above input. Give it a `for` attribute with the value `first` (this should match the above `id` of the element being labeled). Follow this format exactly:

```html
<label for="first">First name
    <input type="text" id="first" name="first" placeholder="Maggie">
</label>
```

3. To make the last name field, copy the above (label and input). Update the following:
    - on the `input` element:
        - `id` value becomes `last`
        - `name` value becomes `last`
        - `placeholder` value becomes `Simpson`
    - on the `label` element:
        - `for` becomes `last` (to match the `id` we just changed)
        - Label text becomes `Last name` (after the label's opening tag)

4. To make the company field, copy the above (label and input). Update the following:
    - on the `input` element:
        - `id` value becomes `company`
        - `name` value becomes `company`
        - `placeholder` value becomes `The Simpsons`
    - on the `label` element:
        - `for` becomes `company` (to match the `id` we just changed)
        - Label text becomes `Company` (after the label's opening tag)

5. Copy the pattern above to create form fields for `street` `number` and `city`. For placeholders, you can use `Evergreen Terrace`, `742` and `Springfield` respectively.

### Providing multiple options

Both ways are worth knowing. They each have their pros and cons.

#### Alternative 1: Using a text input with a datalist

Pros: Allows typing for improved UX.
Cons: Support is limited. No grouping possible yet

6. Using the same pattern as above, create a text input wrapped in a label. Change the following:

    - on the `input` element:
        - `id` value becomes `state`
        - `name` value becomes `state`
        - `placeholder` value becomes `Oregon`
        - add a new attribute `list` with a value of `states` (this will match the `id` of our datalist)
    - on the `label` element:
        - `for` becomes `state` (to match the `id` we just changed)
        - Label text becomes `State&nbsp;/&nbsp;Region` (after the label's opening tag)

7. Add a `datalist` element with an `id` of `states` (should match the `list` attribute of your `input` element above)

Nested between the `datalist` tags, define the following `option` elements:

- `California` (value of `CA`)
- `Colorado` (value of `CO`)
- `Louisiana` (value of `LA`)
- `New York` (value of `NY`)
- `Oregon` (value of `OR`)
- `Texas` (value of `TX`)

Follow this format for all options:

```html
<option value="CA">California</option>
<option value="CO">Colorado</option>
```
