<h1 id="gothinkster-django-realworld-example-app">gothinkster/django-realworld-example-app</h1>

↑ **Parent:** [Django (web-framework)](django-web-framework.md)  
🏷️ **Tags:** [Gothinkster/realworld implementation](gothinkster-realworld-implementation.md)

As of 2021, last updated 2016, and python 3.5 appears to be mandatory or else:
```
RuntimeError: __class__ not set defining 'AbstractBaseUser' as <class 'django.contrib.auth.base_user.AbstractBaseUser'>. Was __classcell__ propagated to type.__new__?
```
which apparently broke in 3.6: [https://stackoverflow.com/questions/41343263/provide-classcell-example-for-python-3-6-metaclass](https://stackoverflow.com/questions/41343263/provide-classcell-example-for-python-3-6-metaclass) and `pyenv` install fails on Ubuntu 20.10, so... fuck. Workarounds at:
- [https://askubuntu.com/questions/1034475/the-python-ssl-extension-was-not-compiled-missing-the-openssl-lib-error-when](https://askubuntu.com/questions/1034475/the-python-ssl-extension-was-not-compiled-missing-the-openssl-lib-error-when)
- [https://stackoverflow.com/questions/52873193/error-the-python-ssl-extension-was-not-compiled-missing-the-openssl-lib-inst](https://stackoverflow.com/questions/52873193/error-the-python-ssl-extension-was-not-compiled-missing-the-openssl-lib-inst)
but am I in the mood considering that the ancient Django version would require an immediate port anyways? Repo is at Django 1.0, while newest is now already Django 3. The Rails one is broken for the same reason. Fuck 2.

## ↑ Ancestors (12)

1. [Django (web-framework)](django-web-framework.md)
2. [Python web framework](python-web-framework.md)
3. [Python library](python-library.md)
4. [Python (programming language)](python-programming-language.md)
5. [List of programming languages](list-of-programming-languages.md)
6. [Programming language](programming-language-split.md)
7. [Software](software-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Gothinkster/realworld implementation](gothinkster-realworld-implementation.md)
