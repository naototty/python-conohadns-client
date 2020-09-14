Python bindings to the ConoHaDNS API (based on Designate API)
=====================================

Original is OpenStack DNS service client based on Designate API

.. image:: https://img.shields.io/pypi/v/python-designateclient.svg
    :target: https://pypi.python.org/pypi/python-designateclient/
    :alt: Latest Version

.. image:: https://img.shields.io/pypi/dm/python-designateclient.svg
    :target: https://pypi.python.org/pypi/python-designateclient/
    :alt: Downloads

This is a client library for Designate built on the Designate API. It
provides a Python API (the ``designateclient`` module) and a command-line tool
(``designate``).

Development takes place via the usual OpenStack processes as outlined in the
`developer guide <http://docs.openstack.org/infra/manual/developers.html>`_.  The master
repository is in `Git <http://git.openstack.org/cgit/openstack/python-designateclient>`_.

See release notes and more at `<http://docs.openstack.org/developer/python-designateclient/>`_.

* License: Apache License, Version 2.0
* `PyPi`_ - package installation
* `Online Documentation`_
* `Bugs`_ - issue tracking
* `Source`_
* `How to Contribute`_

.. _PyPi: https://pypi.python.org/pypi/python-designateclient
.. _Online Documentation: http://docs.openstack.org/developer/python-designateclient
.. _Bugs: https://bugs.launchpad.net/python-designateclient
.. _Source: https://git.openstack.org/cgit/openstack/python-designateclient
.. _How to Contribute: http://docs.openstack.org/infra/manual/developers.html


## python-conohaclient について
=====================================

### PyPIへの登録
-----------------

github上で一通り動くようになってから、登録しようと思います。

なので、しばらく、Designateからのforkという形で開発します。

PyPIについては、初めてなので、ちょっと手こずるかも。

### update
-----------------

* 2020-07-02 リポジトリを "python-conohadnsclient" に renameしました。
* githubの仕様で、しばらくは前の "python-designamteclient" のままでもアクセスできるみたい


### docs
-----------------

markdownではなく、.rstと今更気がついたw


### Issues / Projects
-----------------

Issuesはオリジナルのリポジトリじゃないと使えないのです。

しばらくは、forkプロジェクトとして、こちらで作業します。

* その間は、カンバン方式で、"To do", "In progress", "Done" で管理
* PyPIへのリリース準備のときには、リポジトリを新設して、master branchでアクセスできるようにします
* リリース後には、そちらのIssuesを主体に対応、かなと。




