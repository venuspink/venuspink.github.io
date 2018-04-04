---
layout: post
title: 데이터흐름과 props
category: ReactJS
tags: [ReactJS, jsx, props]
comments: true
---

부모 컴포넌트 하나가 전체 데이터를 갖고 있고 이를 자식 컴포넌트에게 전달 할 수 있다.

~~~javascript
class App extends Component {
  render() {
    return (
      <div className="App">
        <Movie title={movies[0]} poster={posterImage[0]}/>
        <Movie title={movies[1]} poster={posterImage[1]}/>
      </div>
    );
  }
}

class Movie extends Component{
    render(){
        return (
            <div>
                <MoviePoster poster={this.props.poster}/>
                <h1>{this.props.title}</h1>
            </div>
        )
    }
}

class MoviePoster extends Component{
    render() {
        return (
            <img src={this.props.poster}/>
        )
    }
}
~~~







