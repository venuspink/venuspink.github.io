---
layout: post
title: 리액트 컴포넌트와 JSX
category: ReactJS
tags: [ReactJS, jsx]
comments: true
---



이것만 기억하자.

컴포넌트 생성 > 렌더 > 리턴 > html 내용 >> 브라우저 확인

Import React > class 생성 > render() {} 정의 



App.js 안에 Movie컴포넌트가 있고 그 Movie 컴포넌트 안에 MoviePoster 컴포넌트가 들어간다.



JSX? 리액트로 작성하는 html 앱!

### Movie.js

```javascript
import React, {Component} from 'react';
import './Movie.css';

class Movie extends Component{
    render(){
        return (
            <div>
                <MoviePoster />
                <h1>hello this is a movie</h1>
            </div>
        )
    }
}

class MoviePoster extends Component{
    render() {
        return (
            <img src="http://store.hbo.com/imgcache/product/resized/000/506/911/catl/true-detective-touch-darkness-poster-11x17_1000.jpg" />
        )
    }
}

export default Movie;
```

 

### App.js

```javascript
import React, { Component } from 'react';
import logo from './logo.svg';
import './App.css';
import Movie from './Movie';

class App extends Component {
  render() {
    return (
      <div className="App">
        <Movie />
      </div>
    );
  }
}

export default App;
```

