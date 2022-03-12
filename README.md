- 👋 Hi, I’m @little51
I am the author of gitclone.com and classnotfound.com.cn

# gitclone.com
gitclone.com is a github.com cache acceleration website that accelerates the git clone operation from github by caching the frequently accessed github repository. When you clone therepository using git clone https://gitclone.com/github.com/yourrepository, gitclone.com will create a mirror, and when other developer clone in the future, then can use the mirror cache to make the clone. The speed has been greatly improved. Generally, git clone from github can only reach 20k / s. After accelerated by gitclone.com, it can reach 1.2M / s.

The working mechanism of gitclone is: when the developer first proxy the clone project through gitclone.com, gitclone.com mirrors the project asynchronously. When other developer clones the project in the future, it will use the local mirror of gitclone.com instead of Clone from github.com. gitclone.com will synchronize with github.com every night. In order to solve the growing demand for hard disk resources of mirrors, gitclone.com uses a blockchain cluster to expand. Each mirror operation will be broadcast to all servers in the cluster. Each server can choose to generate a mirror and register to respond to subsequent clones. request. At the same time, gitclone.com also explained the accelerated access of stackoverflow.com and go get, so as to “for developers”.

# classnotfound.com.cn
When developing Java applications, it is common to encounter ClassNotFoundException errors, which mean that the specified class cannot be found, and sometimes There will be NoClassDefFoundError errors, which are due to the lack of the corresponding jar package, or the jar package is not placed in a directory recognized by the compiler. The reason for the problem is simple and easy to locate, but it is still difficult to find out which jar is missing simply by the class name. There is a foreign website findjar.com, which implements the function of finding jars through class names, but this website may be due to the large number of visits, the website is often not opened, and the access speed is very slow, so the idea of developing similar websites has been generated.

After a period of development and data collation work, the https://classnotfound.com.cn has been launched, and the source code has been open sourced https://github.com/git-cloner/classnotfound.

https://classnotfound.com.cn Implement the ability to search for jars by class name and jar package name if the keyword is determined by “.” Separated, it is considered to be the class name, otherwise it is the jar package name, and the retrieved jar package can view the historical version and the POM file at the same time.
