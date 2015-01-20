A minimal package to reproduce "dist must be a Distribution instance"

- First started appearing on pip 6.0.6. Some trial and error seems to indicate
  that setuptools 10.0

Example::

    (pbr-test)campbr9:~/git/pbr-test (master) $ python setup.py develop
    running develop
    running egg_info
    writing requirements to Test.egg-info/requires.txt
    writing Test.egg-info/PKG-INFO
    writing top-level names to Test.egg-info/top_level.txt
    writing dependency_links to Test.egg-info/dependency_links.txt
    writing pbr to Test.egg-info/pbr.json
    [pbr] Reusing existing SOURCES.txt
    running build_ext
    Creating /localhome/campbr9/.virtualenvs/pbr-test/lib/python2.7/site-packages/Test.egg-link (link to .)
    Test 0.1.0.dev1 is already the active version in easy-install.pth
    Installed /localhome/campbr9/git/pbr-test
    Processing dependencies for Test==0.1.0.dev1
    Searching for stevedore
    Reading http://example.com/+simple/stevedore/
    Best match: stevedore 1.2.0
    Downloading http://example.com/+f/bd8/2728ab03e6212/stevedore-1.2.0.tar.gz#md5=bd82728ab03e62121fbbb077bcd55fdb
    Processing stevedore-1.2.0.tar.gz
    Writing /tmp/easy_install-_j8MPi/stevedore-1.2.0/setup.cfg
    Running stevedore-1.2.0/setup.py -q bdist_egg --dist-dir /tmp/easy_install-_j8MPi/stevedore-1.2.0/egg-dist-tmp-KsgYnU
    ERROR:root:Error parsing
    Traceback (most recent call last):
      File "/localhome/campbr9/git/pbr-test/.eggs/pbr-0.10.7-py2.7.egg/pbr/core.py", line 104, in pbr
        attrs = util.cfg_to_args(path)
      File "/localhome/campbr9/git/pbr-test/.eggs/pbr-0.10.7-py2.7.egg/pbr/util.py", line 240, in cfg_to_args
        kwargs = setup_cfg_to_setup_kwargs(config)
      File "/localhome/campbr9/git/pbr-test/.eggs/pbr-0.10.7-py2.7.egg/pbr/util.py", line 359, in setup_cfg_to_setup_kwargs
        cmd = cls(dist)
      File "/localhome/campbr9/.virtualenvs/pbr-test/local/lib/python2.7/site-packages/setuptools/__init__.py", line 124, in __init__
        _Command.__init__(self,dist)
      File "/usr/lib/python2.7/distutils/cmd.py", line 58, in __init__
        raise TypeError, "dist must be a Distribution instance"
    TypeError: dist must be a Distribution instance
