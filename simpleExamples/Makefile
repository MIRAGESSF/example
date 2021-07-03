# Package name and version
PACKAGENAME = simpleExamples

# Definitions for the package source directory tree. 
SOURCE = src

# Jar names. 
JARS = $(PACKAGENAME).jar

### Directories ### 

# Where the .java are 
SOURCE = src
SOURCEDIR = $(SOURCE)

# Where the .class are generated 
CLASSESDIR = bin

# where the .jar go
JARSDIR = ../../jars

# where the .java are
SOURCEFILES =  $(addsuffix /*.java, $(SOURCEDIR))

### Tools ###

JAVAC = javac 
COMPILEOPT = -d $(CLASSESDIR)
JAVADOC = javadoc
DOCOPT = -author -version

### COMMANDS FOR DEVELOPMENT ### 
build:
	$(JAVAC) $(COMPILEOPT) $(SOURCEFILES)

buildg:
	$(JAVAC) $(COMPILEOPT) -g $(SOURCEFILES)

clean:
	rm -fr 	$(addsuffix /*.class, $(CLASSESDIR)) \
	       	$(addsuffix /*.java~, $(SOURCEDIR)) \
	       	$(addsuffix /*.class, $(SOURCEDIR)) \
	       	$(addsuffix /TAGS, $(SOURCEDIR))

javadoc:

jar:
	jar -cvf $(JARSDIR)/$(PACKAGENAME).jar -C $(CLASSESDIR) .
