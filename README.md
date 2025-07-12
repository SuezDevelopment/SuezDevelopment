

## Hi there 👋, I'm [Gideon](https://www.linkedin.com/in/gideonolayode/). Welcome to my GitHub Profile!
<p align="center">
  <a href="https://github.com/SuezDevelopment?tab=repositories&sort=stargazers">
    <img alt="total stars" title="Total stars on GitHub" src="https://custom-icon-badges.demolab.com/github/stars/SuezDevelopment?style=for-the-badge&logo=star&date=1112072025"/></a>
  <a href="https://github.com/SuezDevelopment?tab=followers">
    <img alt="followers" title="Follow me on Github" src="https://custom-icon-badges.demolab.com/github/followers/SuezDevelopment?style=for-the-badge&logo=person-add&label=Follow&logoColor=white&date=1112072025"/></a>
  <a href="https://github.com/SuezDevelopment/">
    <img alt="views" title="GitHub profile views" src="https://komarev.com/ghpvc/?username=SuezDevelopment&style=for-the-badge"/></a>
</p>

<p align="center">
<img src="https://github-readme-streak-stats-9m8ugfa77-denvercoder1.vercel.app/?user=SuezDevelopment&theme=transparent&hide_border=true&date=1112072025">

<img src="https://github-readme-stats.vercel.app/api?username=SuezDevelopment&hide_border=true&theme=transparent&date=1112072025">
<img src="https://github-readme-stats.vercel.app/api/top-langs?username=SuezDevelopment&layout=compact&hide_border=true&theme=transparent&date=1112072025">

<img src="https://github-profile-trophy.vercel.app/?username=SuezDevelopment&theme=discord&title=MultiLanguage,Commits,Followers,Stars,Issues,PullRequest,Repositories,Reviews&date=1112072025">

</p>  


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
