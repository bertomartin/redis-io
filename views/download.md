Download
===

Redis uses a standard practice for its versioning:
**major.minor.patchlevel**.
An even **minor** marks a **stable** release, like 1.2, 2.0, 2.2, 2.4, 2.6, 2.8.Odd minors are used for **unstable** releases, for example 2.9.x releases are the unstable versions of what will be Redis 3.0 once stable.

<table class="versions">

  <tr class="current">
    <td>2.8.3</td>
    <td>Stable</td>
    <td>Redis 2.8 provides significant improvements like: Replication partial resynchronization, IPv6 support, config rewriting, keyspace changes notifications via Pub/Sub, and more. See the <a href="https://github.com/antirez/redis/raw/2.8/00-RELEASENOTES">Release Notes</a> for a full list of changes in this release.</td>
    <td>
      <a href="http://download.redis.io/releases/redis-2.8.3.tar.gz">Download</a>
    </td>
  </tr>

  <tr>
    <td>2.6.17</td>
    <td>Old</td>
    <td>This is the newest Redis version replacing Redis 2.4.
    Redis 2.6 features support for <a href="/commands/eval">Lua scripting</a>, milliseconds precision expires, improved memory usage, unlimited number of clients, improved AOF generation, better performance, a number of new commands and features. For the complete list of new features, and the list of fixes contained in each 2.6 release, please check the <a href="https://github.com/antirez/redis/raw/2.6/00-RELEASENOTES">Release Notes</a>.
    <br>
    <td>
      <a href="http://download.redis.io/releases/redis-2.6.17.tar.gz">Download</a>
    </td>
  </tr>

  <tr>
    <td>Unstable</td>
    <td>Unstable</td>
    <td>This is where all the development happens. Only for hard core hackers.
    <td>
      <a href="https://github.com/antirez/redis/tree/unstable">Clone</a>
    </td>
  </tr>

  <tr>
    <td>Win32/64</td>
    <td>Unofficial</td>
    <td>The Redis project does not directly support Windows, however the Microsoft Open Tech group develops and maintains an <a href="https://github.com/MSOpenTech/redis">experimental Windows port targeting Win32/64</a>.

    Currently the port is not production quality but can be used for development purposes on Windows environments. We look forward for collaborating with the authors of this efforts but currently <a href="http://antirez.com/post/redis-win32-msft-patch.html">we will not merge the Windows port</a> to the main code base.
    <td>
      <a href="https://github.com/MSOpenTech/redis">Clone</a>
    </td>
  </tr>

</table>

Other downloads are available on [GitHub](https://github.com/antirez/redis/downloads), Historical downloads are available on [Google Code](http://code.google.com/p/redis/downloads/list?can=1).

**Scripts and other automatic downloads** can easily access the tarball of the latest Redis stable version at <a href="http://download.redis.io/redis-stable.tar.gz">http://download.redis.io/redis-stable.tar.gz</a>. The source code of the latest stable release is [always browsable here](http://download.redis.io/redis-stable), use the file **src/version.h** in order to extract the version in an automatic way.

How to verify files for integrity
===

The Github repository <a href="https://github.com/antirez/redis-hashes/blob/master/README">redis-hashes</a> contains a README file with SHA1 digets of released tarball archives.

Installation
===

Download, extract and compile Redis with:

    $ wget http://download.redis.io/releases/redis-2.8.3.tar.gz
    $ tar xzf redis-2.8.3.tar.gz
    $ cd redis-2.8.3
    $ make

The binaries that are now compiled are available in the `src` directory. Run Redis with:

    $ src/redis-server

You can interact with Redis using the built-in client:

    $ src/redis-cli
    redis> set foo bar
    OK
    redis> get foo
    "bar"

Are you new to Redis? Try our [online, interactive tutorial](http://try.redis-db.com).

Where's Redis Cluster?
---

Redis Cluster, the distributed version of Redis, is making a lot of progresses and you can find a full implementation in the *unstable* branch at Github. It will be released as a release candidate at the end of 2013. You can [watch a video about what Redis Cluster can currently do](https://vimeo.com/63672368).
