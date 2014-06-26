# MicroView Learn 

The MicroView Learn website is generated using Jekyll.  The following open source projects are required to build 
* [Jekyll-Bootstrap] (http://jekyllbootstrap.com)
* [Jekyll Lunr JS Search] (https://github.com/slashdotdash/jekyll-lunr-js-search)
* [Simpleyyt Theme by Yitao] (https://github.com/Simpleyyt/simpleyyt.github.io)

Please feel free to submit pull request for corrections, updates and bug fixes. We appreciate community contributions.

# Building Doxygen documentation

1. Install [Doxygen](http://www.stack.nl/~dimitri/doxygen/).
2. Clone or pull the latest [learn-website-source repo](https://github.com/geekammo/learn-website-source.git) to learn-website-source folder.
3. Clone or pull the lastest [MicroView Library](https://github.com/geekammo/MicroView-Arduino-Library.git) to MicroView folder.
4. Make sure you have the following folder structure:
  * MicroView
  * learn-website-source
5. Change directory to learn-website-source by typing `cd learn-website-source` at the terminal.
6. Type `doxygen _doxyconfig`
7. Doxygen will iterate MicroView folder looking to comment in the CPP and H source code and generate html files in learn-website-source\doco\html
8. Run `jekyll build` like normal.
9. The resulted html files will be stored in learn-website-source\_site
10. Push to Amazon or any web hosting site. 


# Jekyll-Bootstrap

The quickest way to start and publish your Jekyll powered blog. 100% compatible with GitHub pages

## Usage

For all usage and documentation please see: <http://jekyllbootstrap.com>

## Version

0.3.0 - stable and versioned using [semantic versioning](http://semver.org/).

**NOTE:** 0.3.0 introduces a new theme which is not backwards compatible in the sense it won't _look_ like the old version.
However, the actual API has not changed at all.
You might want to run 0.3.0 in a branch to make sure you are ok with the theme design changes.

## Contributing


To contribute to the framework please make sure to checkout your branch based on `jb-development`!!
This is very important as it allows me to accept your pull request without having to publish a public version release.

Small, atomic Features, bugs, etc.
Use the `jb-development` branch but note it will likely change fast as pull requests are accepted.
Please rebase as often as possible when working.
Work on small, atomic features/bugs to avoid upstream commits affecting/breaking your development work.

For Big Features or major API extensions/edits:
This is the one case where I'll accept pull-requests based off the master branch.
This allows you to work in isolation but it means I'll have to manually merge your work into the next public release.
Translation : it might take a bit longer so please be patient! (but sincerely thank you).

**Jekyll-Bootstrap Documentation Website.**

The documentation website at <http://jekyllbootstrap.com> is maintained at https://github.com/plusjade/jekyllbootstrap.com


## License

[MIT](http://opensource.org/licenses/MIT)
