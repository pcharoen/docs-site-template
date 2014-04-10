## docs-site-template

The docs-site-template is a project template for project documents site generator. It uses [Apache Maven Site Plugin](http://maven.apache.org/plugins-archives/maven-site-plugin-3.3/)
to generate a project document site. The site can be configured with a simple [site.xml](http://maven.apache.org/plugins-archives/maven-site-plugin-3.3/examples/sitedescriptor.html)
configuration. The documents can be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) syntax.
It uses Apache Maven site plugin with [Fluido Skin](https://maven.apache.org/skins/maven-fluido-skin/) built on top of [Twitter's Bootstrap 2.2.2]
(http://bootstrapdocs.com/v2.2.2/docs/) web front end framework. The generated site can be deployed on Github project gh-pages branch 
or any web server. [Click here](http://ualbertalib.github.io/docs-site-template) to see a sample site.

### System Requirements

* Java 6 <http://www.oracle.com/technetwork/java/javase/overview/index.html>
* Apache Maven 3 <http://maven.apache.org/>
* Git <http://git-scm.com/>

### Usage

#### Generate project documents 

* create branch gh-pages on your project repository
* clone gh-pages branch

```shell
$ git clone https://github.com/ualbertalib/${project.name}.git -b gh-pages ${project.docs.dir}
```

* clone docs-site-template project

```shell
$ git clone https://github.com/ualbertalib/docs-site-template.git ${docs.site.template.dir}
```

* edit your documents in `${basedir}/src/site/markdown` directory

```
$ cd ${docs.site.template.dir}
```

* generate project documents

```
$ mvn site -Dsite.output.dir=${project.docs.dir}
```

* commit and push to gh-pages branch

```
$ git add .
$ git commit -m "Update project documents"
$ git push
```

#### View project documents

* Point your browser to https://ualbertalib.github.io/${project.name}









