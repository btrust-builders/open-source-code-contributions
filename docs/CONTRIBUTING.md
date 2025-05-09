# Steps to contribute

<img align="right" width="300" src="https://github.com/btrust-builders/open-source-code-contributions/blob/main/assets/fork.png" alt="fork this repository" />

## Fork this repository by clicking on fork button

## Clone your fork of this repository.

In your fork of this repository, click on `Code` button. Select `SSH` tab and then click on `copy to clipboard` button.

<img align="right" width="300" src="https://github.com/btrust-builders/open-source-code-contributions/blob/main/assets/clone.png" alt="clone this repository" />
Open a terminal and run `git clone` command

```bash
git clone "url you copied"
```

> [!IMPORTANT]
> In the following steps, when you see `your-github-username` your should replace it with your GitHub Username.  
> For example, if your GitHub Username is `btrust-builders`,  
> `git switch -c add-your-github-username` becomes `git switch -c add-btrust-builders`  
> `contributors/your-github-username.html` becomes `contributors/btrust-builders.html`

<img align="right" width="300" src="https://github.com/btrust-builders/open-source-code-contributions/blob/main/assets/copy-to-clipboard.png" alt="copy URL to clipboard" />

## Create a branch

Go to the repository directory if you're not already there

```bash
cd open-source-code-contributions
```

Create a branch with `git switch` command

```bash
git switch -c add-your-github-username
```


## Create your card

You can add your card as an HTML file in the contributors directory. Create a file with your Github username in contributors directory. You can copy the following template to get started.

`contributors/your-github-username.html`
```html
<article>
  <h3>Your name</h3>
  <p>A small bio about you</p>
  <h4>Programming languages I use</h4>
  <section class="container">
    <div class="badge" style="background-color: #000000; color: white">Rust</div>
    <div class="badge" style="background-color: #f7df1e; color: black;">JavaScript</div>
  </section>

  <h4>Tools I use</h4>
  <section class="container">
    <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/bash/bash-original.svg"/>
    <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linux/linux-original.svg"/>
  </section>
</article>
<style>
  body {
    font-family: sans-serif;
  }
  .container {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }
  .badge {
    padding: 0.5rem;
    border-radius: 0.25rem;
  }
  .icon {
    width: 2rem;
  }
</style>

```
## Add your card to contributors list

Add the name of the file you created to `scripts/contributors.js` file.

`scripts/contributors.js`
```js
const contributorFiles = [
  "btrust-builders.html",
  "your-github-username.html", // add your file name here
];
```

## View your changes in a web browser

You can see your changes by opening `index.html` in a web browser. You should be able to see the new card you added in the previous steps.

You can continue making changes to your card and refresh the web browser tab to see those changes.

## Commit your changes

First stage your changes with `git add` command

```bash
git add contributors/your-github-username.html
```

Now commit your changes with `git commit` command

```bash
git commit -m "Add your-github-username contributor card"
```

## Push your changes to GitHub

```bash
git push -u origin add-your-github-username
```

## Submit your changes for review

If you go to your repository on GitHub, you'll see a `Compare & pull request` button. Click on that button.

<img style="float: right;" src="https://github.com/btrust-builders/first-open-source-contributions/blob/main/assets/compare-and-pull.png" alt="create a pull request" />

Now submit the pull request.

<img style="float: right;" src="https://github.com/btrust-builders/first-open-source-contributions/blob/main/assets/submit-pull-request.png" alt="submit pull request" />

You will get a notification email once the changes have been merged.
