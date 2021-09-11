# ebiten-signals
A very minimal signal pattern, built for ebiten

## Usage
```go
import signals "github.com/tducasse/ebiten-signals"

params := []interface{}{"string here", "a string"}
// emit a signal from anywhere in your game
signals.Emit("collided", params)

// connect to it somewhere else
signals.Connect("collided", func(i []interface{}) {
  message = ""
  for _, part := range i {
    message += part.(string) + " "
  }
})
```