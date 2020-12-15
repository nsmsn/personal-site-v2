# Being the personal website of one Nick Simson

In late 2020/early 2021 I am going to try rebuilding and relaunching my long-dormant blog with [Eleventy](https://github.com/11ty/eleventy), a static site generator. 


## Starter Files
I'm using the popular [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog) as a starting point, and porting my previous content over, starting with my posts.

* [Netlify](https://eleventy-base-blog.netlify.com/)
* [GitHub Pages](https://11ty.github.io/eleventy-base-blog/)
* [Remix on Glitch](https://glitch.com/~11ty-eleventy-base-blog)
* [Deploy your own starter site on Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/11ty/eleventy-base-blog)
* [Deploy your own starter site on Vercel](https://vercel.com/import/project?template=11ty%2Feleventy-base-blog)


### Implementation Notes

* `about/index.md` shows how to add a content page.
* `posts/` has the blog posts but really they can live in any directory. They need only the `post` tag to be added to this collection.
* Add the `nav` tag to add a template to the top level site navigation. For example, this is in use on `index.njk` and `about/index.md`.
* Content can be any template format (blog posts needn’t be markdown, for example). Configure your supported templates in `.eleventy.js` -> `templateFormats`.
	* Because `css` and `png` are listed in `templateFormats` but are not supported template types, any files with these extensions will be copied without modification to the output (while keeping the same directory structure).
* The blog post feed template is in `feed/feed.njk`. This is also a good example of using a global data files in that it uses `_data/metadata.json`.
* This example uses three layouts:
  * `_includes/layouts/base.njk`: the top level HTML structure
  * `_includes/layouts/home.njk`: the home page template (wrapped into `base.njk`)
  * `_includes/layouts/post.njk`: the blog post template (wrapped into `base.njk`)
* `_includes/postlist.njk` is a Nunjucks include and is a reusable component used to display a list of all the posts. `index.njk` has an example of how to use it.
