# Workshop 1 - Local GIT with Sourcetree

### Basic GIT
0. Create code directory
```
...\GIT
```

1. New repository
    - Open **Sourcetree** 
    - Select `Create Local Repository`
    - Destination path `...\GIT\ws01-git-training`
    - Name `ws01-git-training`
    - Type `Git`

2. Writing your code
    - Open **Visual Studio Code** and browse to `\GIT\ws01-git-training`
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

16. (optional) Merge branch `main` into `feature_style`
    -  To make `feature_style` branch up to date

---

### Work with GitHub

1. Register GitHub
2. New repository name `ws01-git-training`
    - Private repository
    - No need a README file
3. Copy remote URL e.g. `https://github.com/xxx/ws01-git-training.git`
    - Use HTTPS protocal
4. Open `ws01-git-training` local repository in Sourcetree
5. Add new repository path
    - name `origin`
    - path `https://github.com/xxx/ws01-git-training.git`
6. (optional) If `main` branch not exist, rename `master` to `main` branch is required
7. Push `main` branch to remote
8. Checkout `main` branch and update `index.html` then commit as following
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

        <h4>
        GIT push : to upload your local repository content to a remote repository
        </h4>

        <h4>
        Git pull : to update your local repository with the latest changes from a
        remote repository
        </h4>

        <script src="script.js"></script>
    </body>
    </html>
    ```
9. Push `main` branch to remote
10. In GitHub, Add `README.md` file, than commit change
    ```markdown
    # ws01-git-training

    #### This is repository to learn about GIT
    ```
11. In Sourcetree, pull `main` branch from remote to update the branch
    - Use `Fetch` to check what is new
    - Use `Merge` to merge the remote to local branch
    - Use `Pull` to `Fetch` then `Merge` in single action