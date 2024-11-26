# Bluesky Comments For Quarto


# Installing

``` bash
quarto add gadenbuie/quarto-bluesky-comments
```

This will install the extension under the `_extensions` subdirectory. If
you’re using version control, you will want to check in this directory.

## Using

Adding Bluesky-powered comments to your blog is a three-step
process[^1]:

1.  Publish the blog post and post about it on Bluesky.
2.  Copy the link to the Bluesky post.
3.  Add `{{< bluesky-comments {post-url} >}}` to your blog post and
    re-publish.

Using Bluesky for comments introduces a chicken-or-egg problem. You need
one Bluesky post to watch for replies, which will be shown in your blog
post. But to publish that post, you first need to publish your blog. And
then you need to come back to your blog and update it with the link to
the Bluesky post.

The `{{< bluesky-comments >}}` shortcode doesn’t add any additional
decoration (to make it as flexible as possible for your use case).
Here’s a short snippet that adds the comments under a horizontal rule
and in a “Comments” section:

``` markdown
---

## Comments

{{< bluesky-comments https://bsky.app/profile/grrrck.xyz/post/3lbu5opiixc2j >}}
```

[^1]: Yes, I know, that’s actually 5 steps.
