---
created: 2023-07-02 21:03
aliases: 
- add a button to product page to share the product
tags:
- 
cssclasses:
- 
publish:
---

<!-- 
tags: 
-->

<!--internal
parent:: [[]]
child:: [[]]
related:: [[]]
-->

<!--external
- []()
-->

# Add a button to product page to share the product

From a technical standpoint, implementing this change (i.e. adding this button) can take a bit of time

- we might have to design a component that matches the website
- we might have to incorporate it into a template so it shows up on multiple pages 
- we have to explore how the APIs of external social media platforms work
- we might have to require login first or account creation, which would require interacting with a database

we can use Generative AI to write the (straightforward) code to make this happen 

Ask ChatGPT to write a simple Next.js component that implements these social share buttons

```
write a Next.js component that contains buttons to share the current page on social media
```

![[notes/images/Pasted image 20230702212152.png]]

The main human work that would need to be done is review. 

Note that the model even gives an explanation of the code which would make the review time even quicker

we can go further and ask the model to add style to our component using some specific tools in our stack

![[notes/images/Pasted image 20230702212238.png]]

```js
import { useRouter } from 'next/router';
import { makeStyles } from '@material-ui/core/styles';
import Button from '@material-ui/core/Button';

const useStyles = makeStyles((theme) => ({
  button: {
    margin: theme.spacing(1),
    boxShadow: 'none',
    '&:hover': {
      boxShadow: theme.shadows[4],
    },
  },
}));

const ShareButtons = () => {
  const router = useRouter();
  const pageUrl = `https://yourwebsite.com${router.asPath}`;
  const classes = useStyles();

  const shareOnTwitter = () => {
    window.open(`https://twitter.com/intent/tweet?url=${pageUrl}`);
  };

  const shareOnFacebook = () => {
    window.open(`https://www.facebook.com/sharer/sharer.php?u=${pageUrl}`);
  };

  const shareOnLinkedIn = () => {
    window.open(`https://www.linkedin.com/sharing/share-offsite/?url=${pageUrl}`);
  };

  return (
    <div>
      <Button variant="contained" color="primary" className={classes.button} onClick={shareOnTwitter}>
        Share on Twitter
      </Button>
      <Button variant="contained" color="primary" className={classes.button} onClick={shareOnFacebook}>
        Share on Facebook
      </Button>
      <Button variant="contained" color="primary" className={classes.button} onClick={shareOnLinkedIn}>
        Share on LinkedIn
      </Button>
    </div>
  );
};

export default ShareButtons;
```

with solid domain knowledge and good prompt engineering principles, a human can use Generative AI to truncate the time required to implement such a feature

This is a simple example to communicate the essential idea outlined above. The actual task is not complicated, but **that’s the point**.

A lot of the work that leads to valuable business outcomes is not complicated, and Generative AI can be used to expedite the implementation of these changes

The bottom line is that **generative AI makes it fast and easier to implement ideas**