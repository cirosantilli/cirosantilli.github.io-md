<h1 id="codaisseur-feathersjs-react-redux-ssr">Codaisseur/feathersjs-react-redux-ssr</h1>

↑ **Parent:** [FeatherJS demo apps](featherjs-demo-apps.md)

[https://github.com/Codaisseur/feathersjs-react-redux-ssr](https://github.com/Codaisseur/feathersjs-react-redux-ssr)

Also [webpack](webpack-split.md) and [Babel](babel-transcompiler.md), looks promising!

As of 2021, last commit from 2017.

Running:
```
git clone https://github.com/Codaisseur/feathersjs-react-redux-ssr
cd feathersjs-react-redux-ssr
npm install
```
failed on Ubuntu 20.10 [Node.js](node-js-split.md) v14.15.3 with:
```
../src/create_string.cpp:17:37: error: no matching function for call to ‘v8::String::Utf8Value::Utf8Value(v8::Local<v8::Value>&)’
   17 |   v8::String::Utf8Value string(value);
      |                                     ^
```
Likely similar [bullshit](bullshit.md) from: [https://stackoverflow.com/questions/50111688/node-sqlite-node-gyp-build-error-no-member-named-forceset-in-v8object](https://stackoverflow.com/questions/50111688/node-sqlite-node-gyp-build-error-no-member-named-forceset-in-v8object) because the Node.js version is too new.

If I try `nvm install v10`

I [Google](google-split.md) error messages until reaching:
```
diff --git a/gulpfile.js b/gulpfile.js
index b931e06..24d2cc8 100644
--- a/gulpfile.js
+++ b/gulpfile.js
@@ -14,34 +14,34 @@ gulp.task('css', function() {
            .pipe(gulp.dest('./dist'))
 })
 
-gulp.task('css:watch', ['css'], function() {
+gulp.task('css:watch', gulp.series('css', function() {
   gulp.watch('app/styles/**/*.sass', ['css'])
-})
+}))
 
 gulp.task('moveAssets', function() {
   return gulp.src('./app/assets/**/*')
              .pipe(gulp.dest('./dist/assets'))
 })
 
-gulp.task('build:revAssets', ['css', 'moveAssets'], function() {
+gulp.task('build:revAssets', gulp.series('css', 'moveAssets', function() {
   var rev = new $.revAll()
   return gulp.src('./dist/**/*')
              .pipe(rev.revision())
              .pipe(gulp.dest('./dist/public'))
              .pipe(rev.manifestFile())
              .pipe(gulp.dest('./dist'))
-})
+}))
 
 gulp.task('build:cpServer', function() {
   return gulp.src('./app/**/*.{js,ejs}')
              .pipe(gulp.dest('./dist/server-build'))
 })
-gulp.task('build:revServer', ['build:cpServer'], function() {
+gulp.task('build:revServer', gulp.series('build:cpServer', function() {
   var manifest = gulp.src('./dist/rev-manifest.json')
   return gulp.src('./dist/server-build/{components,containers}/**/*')
              .pipe($.revReplace({ manifest: manifest }))
              .pipe(gulp.dest('./dist/server-build'))
-})
+}))
 
 gulp.task('build', function() {
   runSequence('build:revAssets', 'build:revServer')
diff --git a/package.json b/package.json
index bcb29c3..86bd593 100644
--- a/package.json
+++ b/package.json
@@ -67,7 +67,7 @@
     "redux-thunk": "^0.1.0",
     "request": "^2.79.0",
     "rewire": "^2.3.4",
-    "run-sequence": "^1.2.2",
+    "run-sequence": "^2.2.1",
     "serve-favicon": "^2.3.2",
     "socket.io-client": "^1.7.2",
     "superagent": "^1.4.0",
@@ -86,16 +86,16 @@
     "concurrently": "^2.0.0",
     "cross-env": "^1.0.7",
     "enzyme": "^2.3.0",
-    "gulp": "^3.9.0",
+    "gulp": "^4.0.2",
     "gulp-autoprefixer": "^3.1.0",
     "gulp-load-plugins": "^1.2.0",
     "gulp-rev": "^6.0.1",
-    "gulp-sass": "^2.1.1",
+    "gulp-sass": "4.1.0",
     "gulp-sourcemaps": "^1.6.0",
     "jsdom": "^7.0.1",
     "mocha": "^2.4.5",
     "nock": "^2.17.0",
-    "node-sass": "^3.4.2",
+    "node-sass": "^5.0.0",
     "nodemon": "^1.6.0",
     "react-addons-test-utils": "^15.3.2",
     "react-transform-catch-errors": "^1.0.0",
```
and the next problem is: [https://stackoverflow.com/questions/48513573/gulp-error-gulp-hastask-is-not-a-function](https://stackoverflow.com/questions/48513573/gulp-error-gulp-hastask-is-not-a-function)

## ↑ Ancestors (13)

1. [FeatherJS demo apps](featherjs-demo-apps.md)
2. [FeathersJS](feathersjs.md)
3. [Node.js web framework](node-js-web-framework.md)
4. [Node.js](node-js-split.md)
5. [JavaScript](javascript.md)
6. [List of programming languages](list-of-programming-languages.md)
7. [Programming language](programming-language-split.md)
8. [Software](software-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [feathers-chat-react](feathers-chat-react.md)
