
### ✅ Bootstrap Form Syntaxes & Use Cases

1. **Basic Label + Input**

   ```html
   <label for="email" class="form-label">Email</label>
   <input type="email" id="email" class="form-control">
   ```

   🔹 Use when you want a **normal input field with a label**.

---

2. **Readonly Input**

   ```html
   <input type="text" value="lakshmi.com" readonly class="form-control">
   ```

   🔹 Use when you want to **display text that cannot be changed**.

---

3. **Select Dropdown**

   ```html
   <select class="form-select form-select-lg">
     <option>lakshmi</option>
     <option>nidhishree</option>
     <option>sachin</option>
   </select>
   ```

   🔹 Use for **dropdown options** (single selection).

---

4. **Checkbox**

   ```html
   <input type="checkbox" class="form-check-input"> Option
   ```

   🔹 Use for **on/off multiple selections**.

---

5. **Switch (toggle style)**

   ```html
   <div class="form-check form-switch">
     <input class="form-check-input" type="checkbox" role="switch">
   </div>
   ```

   🔹 Use for a **toggle switch instead of a plain checkbox**.

---

6. **Input Group (with symbols / addons)**

   ```html
   <div class="input-group">
     <span class="input-group-text">$</span>
     <input type="number" class="form-control">
     <span class="input-group-text">.00</span>
   </div>
   ```

   🔹 Use to **add symbols/icons before or after input**.

---

7. **Floating Label**

   ```html
   <div class="form-floating">
     <input type="email" id="email" class="form-control" placeholder="Email">
     <label for="email">Email</label>
   </div>
   ```

   🔹 Use for **modern floating labels inside input fields**.

---

8. **Button**

   ```html
   <button type="submit" class="btn btn-primary">Submit</button>
   ```

   🔹 Use `btn btn-primary` for a **Bootstrap styled button**.


   // TABLE
   Perfect Lakshmi 🙌 — you’ve now built a **Bootstrap styled table** with all the right elements! Let me quickly explain each **syntax + use case** so you can remember them clearly:

---

### 🔎 Code Explanation

1. **Responsive Table Wrapper**

```html
<div class="table-responsive">
```

✅ Makes the table **scroll horizontally on small screens** (important for mobile).

---

2. **Bootstrap Table Base Class**

```html
<table class="table">
```

✅ The main Bootstrap table class — adds spacing, padding, and base styling.

---

3. **Extra Table Classes**

* `table-bordered` → Adds borders around all cells.
* `table-hover` → Highlights row when hovered.
* `table-danger` → Makes the table background red-tinted (danger theme).

Example:

```html
<table class="table table-bordered table-hover table-danger">
```

---

4. **Table Header Styling**

```html
<thead class="table-dark">
```

✅ Makes header row have a **dark background with white text**.

---

5. **Row Group Divider**

```html
<tbody class="table-group-divider">
```

✅ Adds a **horizontal dividing line** between rows for clarity.

---

6. **Table Content**

```html
<tr>
  <td>Lakshmi</td>
  <td>K</td>
  <td>21</td>
</tr>
```

✅ Normal row data inside `<tbody>`.

---

### 🚀 Quick Syntax Cheat Sheet (Bootstrap Table)

| Syntax                | Use Case                            |
| --------------------- | ----------------------------------- |
| `table`               | Base Bootstrap table                |
| `table-bordered`      | Adds borders                        |
| `table-striped`       | Adds zebra stripes                  |
| `table-hover`         | Highlight row on hover              |
| `table-dark`          | Dark themed header/body             |
| `table-danger`        | Red tinted table (contextual)       |
| `table-responsive`    | Makes table scroll on small screens |
| `table-group-divider` | Divider between rows                |

---

👉 If you combine these, you can build **professional-looking tables** very fast.

Would you like me to show you how to add **row colors individually** (like only making one row `table-success` and another `table-warning`)?


---

👉 If you **remember just these 8 syntaxes**, you can build **any kind of Bootstrap form**.

Would you like me to create a **cheat sheet table (syntax + screenshot of output + use case)** so you can revise it faster?
