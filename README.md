# HyperCoreAnsibleCollection-docs

Contains a built html documentation for https://github.com/ScaleComputing/HyperCoreAnsibleCollection.
The ./docs subdirectory is deployed by github pages.

Steps:
```
(cd .../ansible_collections/scale_computing/hypercore && make docs)
rm -fr HyperCoreAnsibleCollection-docs/docs
cp -a .../ansible_collections/scale_computing/hypercore/docs/build/html HyperCoreAnsibleCollection-docs/docs
touch HyperCoreAnsibleCollection-docs/docs/.nojekyll
# commit to gh-pages branch, push
# Go to github.com, select this project, then settings, pages, deploy-from-branch, branch=gh-pages, directory=/docs
# remove main branch, keep only gh-pages
```
