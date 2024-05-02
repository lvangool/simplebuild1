# simplebuild1
testing preview functions

```
  simple1:
    git_url: https://github.com/lvangool/simplebuild1.git
    git_branch: main
    ports:
    - container: 8050
      http: 80
      https: 443
    command: "/go/src/app/app --port=8050 --dport=8051 --dip=simple2.sampler"
  simple2:
    git_url: https://github.com/lvangool/simplebuild2.git
    git_branch: main
    ports:
    - container: 8051
      http: 8080
      https: 8443
    command: "/go/src/app/app --port=8051 --dport=8050 --dip=simple1.sampler"
```
