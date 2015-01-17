---
title:script test
layout: post
---
bash script works fine, creating the file with req font matter and opening to eof in vi
````
    # makes a new post for the jekyll blogging platform and opens it
    #use in _posts folder; chmod +x it (obviously)
    echo "enter post name, do not use _ or any other special characters"
    read post_name
    touch `date "+%Y-%m-%d-"`$post_name.markdown
    echo -e "---\ntitle:$post_name\nlayout: post\n---\n" >>  `date "+%Y-%m-%d-"`$post_name.markdown
    #open to line of file after the font matter
    change number if num of font matter lines chages
    vi +5 `date "+%Y-%m-%d-"`$post_name.markdown
````

