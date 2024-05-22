

## Hi there 👋, I'm [Gideon](https://www.linkedin.com/in/gideonolayode/). Welcome to my GitHub Profile!
<div align="center">
	
![Success Alaska Development](/76E2255F-BB27-43D9-A432-825851F46496.png)

</div>

[![Profile views](https://komarev.com/ghpvc/?username=SuezDevelopment&label=Profile%20views&style=for-the-badge)](https://github.com/SuezDevelopment)

---

## 🛠️ Languages and tools
</br>

[![Languages and Tools](https://skillicons.dev/icons?i=androidstudio,cloud,bash,vscode,docker,git,github,linux,heroku,arduino,redis,mongodb,go,java,html,py,c,ts,js,deno,flutter,fastapi&perline=10)](https://www.linkedin.com/in/gideonolayode/)

---

---

## 👨‍💻 LOC
[![Lines of Code](https://api.githubtrends.io/user/svg/SuezDevelopment/langs?time_range=one_year&include_private=True&loc_metric=changed&theme=dark)](https://www.linkedin.com/in/gideonolayode/)

---


<p align="left"> <a href="https://github.com/ryo-ma/github-profile-trophy"><img src="https://github-profile-trophy.vercel.app/?username=SuezDevelopment&theme=dark#gh-dark-mode-only" alt="SuezDevelopment" /></a> </p>

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=SuezDevelopment&show_icons=true&locale=en&layout=compact&theme=dark#gh-dark-mode-only" alt="SuezDevelopment" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=SuezDevelopment&hide=contribs,prs&count_private=true&show_icons=true&locale=en&theme=dark#gh-dark-mode-only&hide=contribs,prs" alt="SuezDevelopment" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=SuezDevelopment&theme=dark#gh-dark-mode-only" alt="SuezDevelopment" /></p>

********
## 2023 ToDo List 
- [x] Create Tutorials in GoLang
- [x] Create Tutorials in Ruby


- Python
```python
def my_function(x: int, y: int) -> int:
    return x / y

result = my_function(360, 30)
print(result) 

```

- Go
```go
/*
The "Feature" function creates a goroutine to execute the wrapped function asynchronously, 
while the returned function waits for the execution to complete before returning the result.
*/
func Feature(f func(interface{}, error)) func() (interface{}, error) {
	var result interface{}
	var err error

	c := make(chan struct{}, 1)
	go func() {
		defer close(c)

		result, err = f()
	}()

	return func() (interface{}, error) {
		<-c
		return result, err
	}
}

```


>## Gideon Olayode
