# Project Euler problem zero

↑ **Parent:** [Bonus Project Euler problem](bonus-project-euler-problem.md)

This was a registration [CAPTCHA](captcha.md) problem as of 2025:

> Among the first 510 thousand square numbers, what is the sum of all the odd squares?

Bash + [Python](python-programming-language.md) "one-liner":
```
python -c $'import sys;max=int(sys.argv[1]) + 1;s = 0\nfor i in range(1, max, 2):\n s += i*i\nprint(s)' 510000
```

With indentation:
```
s = 0
for i in range(1, 510001, 2):
    s += i*i
print(s)
```

As a file at: [euler/0.py](euler/0.py)

## ↑ Ancestors (14)

1. [Bonus Project Euler problem](bonus-project-euler-problem.md)
2. [Main Project Euler problem](main-project-euler-problem.md)
3. [Project Euler problem](project-euler-problem.md)
4. [Project Euler](project-euler-split.md)
5. [Competitive programming website](competitive-programming-website.md)
6. [Competitive programming](competitive-programming.md)
7. [Knowledge olympiad by domain of knowledge](knowledge-olympiad-by-domain-of-knowledge.md)
8. [Knowledge olympiad](knowledge-olympiad.md)
9. [STEM prize](stem-prize.md)
10. [Prize](prize.md)
11. [Social technology](social-technology-split.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)
