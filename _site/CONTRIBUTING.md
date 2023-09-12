
# Contribution Guidelines

Thank you for considering contributing to our open-source programming blog. We welcome contributions from fellow developers and enthusiasts to help us create valuable content for the community. To ensure a smooth collaboration, please follow these guidelines when submitting your contribution:

## Getting Started
- **Make sure you have installed all Jekyll Prerequisites**

- **Fork the Repository:** Begin by forking our blog's GitHub repository to your own GitHub account.

- **Clone the Repository:** Clone your forked repository to your local machine

- **cd into cloned repository :**
  ```
  cd hackers_hive
  ```

- **Create a New Branch:** Before making any changes, create a new branch for your contribution:
  ```bash
  git checkout -b your-branch-name

## Writing a Blog Post
- **Blog Post Format:** Blog posts should be written in Markdown format. Create a new Markdown file in the _posts directory following the naming convention 
```
YYYY-MM-DD-title-of-your-post.md
```
- **Front Matter:** Include Front Matter at the beginning of your Markdown file with metadata like the post's title, subtitle, categories, tags, author, and a banner image. Here's an example:
```
  ---
  layout: post
  title: <Your Blog Post Title>
  subtitle: <short subtitle of your post>
  categories: <category as mentioned in the issue >
  tags: [tags separated by commas]
  author: Your name 
  banner:
      image: assets/images/banners/<imagename.extension>
      heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
      subheading_style: "color: gold"
  ---

```
- **categories, tags will be given in the description of the issue**
- **After opening the pull request maintainers will verify the post and inform if any changes needed**

- **Content:** Write your blog post content in Markdown below the Front Matter. You can include text, code snippets, images, and links.

- **Images:** If your post includes images, place them in the assets/images directory.

- **Testing Locally:** To preview your blog post locally, run jekyll serve and open your browser at http://localhost:4000. Ensure your post renders correctly.
## Submitting Your Contribution
- **Commit Your Changes:** After writing and testing your blog post, commit your changes to your branch:

``` 
git add -A
git commit -m "Add: Your Blog Post Title"
```

- **Push to Your Repository:** Push your changes to your forked repository:

```
git push origin your-branch-name
```

- **Create a Pull Request:** Go to the original repository and create a Pull Request (PR) from your forked branch. Provide a descriptive title and details about your contribution.

- **Review and Discussion:** Participate in the review process by responding to comments, addressing feedback, and making necessary revisions.

## Code of Conduct

Please adhere to our [Code of Conduct](https://github.com/Grimm-s-Alchemy-Chamber/hackers_hive/blob/main/CodeOfConduct.md) in all interactions related to this project.

Thank you for contributing to our open-source programming blog. Your contributions help us create a valuable resource for programmers worldwide!
