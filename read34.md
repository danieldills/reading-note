# React 4

[Dynamic Routes](https://nextjs.org/learn/basics/dynamic-routes)
[Depolyment](https://nextjs.org/learn/basics/deploying-nextjs-app)

How to Statically Generate Pages with Dynamic Routes
In our case, we want to create dynamic routes for blog posts:

We want each post to have the path /posts/<id>, where <id> is the name of the markdown file under the top-level posts directory.
Since we have ssg-ssr.md and pre-rendering.md, we’d like the paths to be /posts/ssg-ssr and /posts/pre-rendering.
Overview of the Steps
We can do this by taking the following steps. You don’t have to make these changes yet — we’ll do it all on the next page.

First, we’ll create a page called [id].js under pages/posts. Pages that begin with [ and end with ] are dynamic routes in Next.js.

In pages/posts/[id].js, we’ll write code that will render a post page — just like other pages we’ve created.

```javascript
import Layout from "../../components/layout";

export default function Post() {
  return <Layout>...</Layout>;
}
```

Now, here’s what’s new: We’ll export an async function called getStaticPaths from this page. In this function, we need to return a list of possible values for id.

```javascript
import Layout from "../../components/layout";

export default function Post() {
  return <Layout>...</Layout>;
}

export async function getStaticPaths() {
  // Return a list of possible value for id
}
```

Finally, we need to implement getStaticProps again - this time, to fetch necessary data for the blog post with a given id. getStaticProps is given params, which contains id (because the file name is [id].js).

```javascript
import Layout from "../../components/layout";

export default function Post() {
  return <Layout>...</Layout>;
}

export async function getStaticPaths() {
  // Return a list of possible value for id
}

export async function getStaticProps({ params }) {
  // Fetch necessary data for the blog post using params.id
}
```

Deploying Your Next.js App

Push to GitHub
Before we deploy, let’s push our Next.js app to GitHub if you haven’t done so already. This will make deployment easier.

On your personal GitHub account, create a new repository called nextjs-blog.
The repository can be public or private. You do not need to initialize it with a README or other files.
If you need help setting up your repo, take a look at this guide on GitHub.
Then:

If you haven’t initialized the git repository locally for your Next.js app, do so now.
Push the Next.js app to your GitHub repository.
To push to GitHub, you can run the following commands (replace <username> with your GitHub username):

```bash
git remote add origin https://github.com/<username>/nextjs-blog.git
git push -u origin main
```

Deploy to Vercel
The easiest way to deploy Next.js to production is to use the Vercel platform developed by the creators of Next.js.

Vercel is a serverless platform for static and hybrid applications built to integrate with your headless content, commerce, or database. We make it easy for frontend teams to develop, preview, and ship delightful user experiences, where performance is the default. You can start using it for free — no credit card required.

Create a Vercel Account
First, go to https://vercel.com/signup to create a Vercel account. Choose Continue with GitHub and go through the sign up process.

Import your nextjs-blog repository
Once you’re signed up, import your nextjs-blog repository on Vercel. You can do so from here: https://vercel.com/import/git.

You’ll need to Install Vercel for GitHub. You can give it access to All Repositories.
Once you’ve installed Vercel, import nextjs-blog.
You can use default values for the following settings — no need to change anything. Vercel automatically detects that you have a Next.js app and chooses optimal build settings for you.

Project Name
Root Directory
Build Command
Output Directory
Development Command
When you deploy, your Next.js app will start building. It should finish in under a minute.

Help is available: If your deployment fails, you can always get help on GitHub Discussions. To learn more about deployment, take a look at our documentation.

When it’s done, you’ll get deployment URLs. Click on one of the URLs and you should see the Next.js starter page live.

Congratulations! You just deployed your Next.js app to production. On the next page, we’ll go into the details of Vercel and the recommended workflow.
