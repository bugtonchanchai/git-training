# Workshop 1 - Local GIT with Sourcetree

### Basic GIT
0. Create code directory
```
...\GIT\local
```

1. New repository
    - Open **Sourcetree** 
    - Select `Create Local Repository`
    - Destination path `...\GIT\local\ws01-localgit`
    - Name `ws01-localgit`
    - Type `Git`

2. Writing your code
    - Open **Visual Studio Code** and browse to `\GIT\local\ws01-localgit`
    - Create `index.html` and write a simple HTML code by using `!`
        ```html
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Document</title>
        </head>
        <body>
            
        </body>
        </html>
        ```

3. Add your code to staging area
    - Goto **Sourcetree**
    - Navigate to `Workspace > File Status`
    - Press `Stage All` button

4. Commit to repository
    - Input commit message
    - Press `Commit` button

5. Edit `index.html` as following
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Index</title>
    </head>
    <body>
        <h1>Hello GIT</h1>
        <p>This is the first file in my new Git Repo.</p>

    </body>
    </html>
    ```
6. Add file to staging area and commit change

7. New file `script.js`
    ```javascript
    const msgSpan = document.getElementById('msg');
    msgSpan.textContent = "This message from script.js";
    ```

8. Update `index.html` as following
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Index</title>
    </head>
    <body>
        <h1>Hello GIT</h1>
        <p>This is the first file in my new Git Repo.</p>

        <span id="msg"></span>

        <script src="script.js"></script>
    </body>
    </html>
    ```

9. Add file to staging area and commit change

---

### GIT Branch & Merge
1. Create new branch `feature_style` from latest commit, than switch to this branch

2. New file `style.css`
    ```css
    body {
        font-family: Arial, sans-serif;
        background-color: #f0f0f0;
        margin: 0;
        padding: 20px;
    }

    h1 {
        color: #333;
    }

    p {
        font-size: 18px;
        color: #666;
    }

    #msg {
        display: block;
        margin-top: 20px;
        font-weight: bold;
        color: #007bff;
    }
    ```

3. Update `index.html` as following
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Index</title>
        <link rel="stylesheet" href="style.css" />
    </head>
    <body>
        <h1>Hello GIT</h1>
        <p>This is the first file in my new Git Repo.</p>

        <span id="msg"></span>

        <script src="script.js"></script>
    </body>
    </html>
    ```

4. Add file to staging area and commit change

5. Update `style.css` by increase font-size to 20px as following
    ```css
    body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    padding: 20px;
    }

    h1 {
    color: #0219c7;
    }

    p {
    font-size: 20px;
    color: #666;
    }

    #msg {
    display: block;
    margin-top: 20px;
    font-weight: bold;
    color: #007bff;
    }
    ```

6. Add file to staging area and commit change

7. Checkout `main` branch

8. Merge branch `feature_style` into `main`
    - This case `main` has no change

9. Checkout `feature_style` branch

10. Update `style.css` by add `text-align: center;` into `body` as following
    ```css
    body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    padding: 20px;
    text-align: center;
    }

    h1 {
    color: #0219c7;
    }

    p {
    font-size: 20px;
    color: #666;
    }

    #msg {
    display: block;
    margin-top: 20px;
    font-weight: bold;
    color: #007bff;
    }
    ```

11. Add file to staging area and commit change

12. Checkout `main` branch

13. Update `index.html` by add `<hr>` and `<h3>` tag as following
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Index</title>
        <link rel="stylesheet" href="style.css" />
    </head>
    <body>
        <h1>Hello GIT</h1>
        <p>This is the first file in my new Git Repo.</p>

        <span id="msg"></span>

        <hr />

        <h3>This message from main branch</h3>

        <script src="script.js"></script>
    </body>
    </html>
    ```

14. Add file to staging area and commit change

15. Merge branch `feature_style` into `main`
    - This case `main` have change