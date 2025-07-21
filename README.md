

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

def feature(f: Callable[[], Tuple[Any, Exception]]) -> Callable[[], Tuple[Any, Exception]]:
    """
    Wraps a function to run asynchronously in a thread and returns a closure to get the result.
    """
    result = [None, None]  # [result, error]
    done = threading.Event()

    def run():
        try:
            result[0], result[1] = f()
        finally:
            done.set()

    threading.Thread(target=run, daemon=True).start()

    def get_result() -> Tuple[Any, Exception]:
        done.wait()
        return result[0], result[1]

    return get_result

def retryable(call: Callable[[], Exception], max_retries: int, backoff: float) -> Exception:
    """
    Executes a function with exponential backoff retries.
    backoff is in seconds (float).
    """
    if max_retries == 0:
        return call()

    delay = backoff
    for i in range(max_retries + 1):
        err = call()
        if err is not None:
            if i == max_retries:
                return err
            time.sleep(delay)
            delay *= 2
            continue
        return None
    return None

```

- Go
```go

// Retryable executes a function with exponential backoff retry logic
func Retryable(call func() error, max int, backoff time.Duration) error {
	if max == 0 {
		return call()
	}

	for i := 0; i <= max; i++ {
		if err := call(); err != nil {
			if i == max {
				return err
			}
			time.Sleep(backoff)
			backoff *= 2
			continue
		}
		return nil
	}
	return nil
}

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
- Rust
```rust

fn feature<F, T, E>(f: F) -> impl FnOnce() -> Result<T, E>
where
    F: FnOnce() -> Result<T, E> + Send + 'static,
    T: Send + 'static,
    E: Send + 'static,
{
    let (tx, rx): (mpsc::Sender<Result<T, E>>, mpsc::Receiver<Result<T, E>>) = mpsc::channel();
    
    thread::spawn(move || {
        let result = f();
        let _ = tx.send(result);
    });

    move || rx.recv().unwrap()
}

fn retryable<F, E>(call: F, max: usize, backoff: Duration) -> Option<E>
where
    F: Fn() -> Option<E>,
{
    if max == 0 {
        return call();
    }

    let mut delay = backoff;
    for _ in 0..=max {
        if let Some(err) = call() {
            if _ == max {
                return Some(err);
            }
            thread::sleep(delay);
            delay *= 2;
            continue;
        }
        return None;
    }
    None
}
```

>## Gideon Olayode
