---
id: 221
title: How do I exclude paths in gulp?
date: 2017-03-03T05:08:53+00:00
author: admin
layout: post
permalink: /blog/20170303/how-to-exclude-paths-gulp/
categories:
  - Web Development
---

One of the things that's nice about gulp is that you can easily exclude paths when specifying the paths you would like to include by adding an exclamation before the path. The task below will include all scss files except if they are in the folder partials, since those will be included as needed.

<pre>
gulp.task('sass', function () {
  return gulp.src('src/sass/**/*.scss', '!src/sass/partials/*.sass')
    .pipe(sass().on('error', sass.logError))
    .pipe(gulp.dest('./public/css'));
});
</pre>
