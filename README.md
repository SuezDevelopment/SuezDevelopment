

### Hi there 👋, welcome!


![Success Alaska Development](/76E2255F-BB27-43D9-A432-825851F46496.png)

# **SuezDevelopment** 
<p align="left"> <img src="https://komarev.com/ghpvc/?username=SuezDevelopment&label=Profile%20views&color=0e75b6&style=flat" alt="jemmycodes" /> </p>

<p align="left"> <a href="https://github.com/ryo-ma/github-profile-trophy"><img src="https://github-profile-trophy.vercel.app/?username=SuezDevelopment" alt="SuezDevelopment" /></a> </p>

********
## 2023 ToDo List 
- [x] Create Tutorials in GoLang
- [x] Create Tutorials in Ruby

## Contact

- Email: [olayode.gideon@calebuniversity.edu.ng](mailto:olayode.gideon@calebuniversity.edu.ng)
- LinkedIn: [linkedin.com/in/gideonolayode](https://www.linkedin.com/in/gideonolayode/)

[1.2]: http://i.imgur.com/wWzX9uB.png
- Twitter: [![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/giddy1billion.svg?style=social&label=Follow%20%40giddy1billion)](https://twitter.com/giddy1billion)


```python
def my_function(x: int, y: int) -> int:
    return x / y

result = my_function(360, 30)
print(result) 

```



// 

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


<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=SuezDevelopment&show_icons=true&locale=en&layout=compact" alt="SuezDevelopment" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=SuezDevelopment&show_icons=true&locale=en" alt="SuezDevelopment" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=SuezDevelopment&" alt="SuezDevelopment" /></p>


>## Gideon Olayode
