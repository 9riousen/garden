---
title: "Download npm package in tar.gz"
date: '2022-11-27'
---
```bash
% npm pack react
npm notice 
npm notice 📦  react@18.2.0
npm notice === Tarball Contents === 
npm notice 1.1kB   LICENSE                                    
npm notice 1.2kB   README.md                                  
npm notice 41.1kB  cjs/react-jsx-dev-runtime.development.js   
npm notice 343B    cjs/react-jsx-dev-runtime.production.min.js
npm notice 342B    cjs/react-jsx-dev-runtime.profiling.min.js 
npm notice 41.7kB  cjs/react-jsx-runtime.development.js       
npm notice 859B    cjs/react-jsx-runtime.production.min.js    
npm notice 858B    cjs/react-jsx-runtime.profiling.min.js     
npm notice 87.6kB  cjs/react.development.js                   
npm notice 6.9kB   cjs/react.production.min.js                
npm notice 501B    cjs/react.shared-subset.development.js     
npm notice 351B    cjs/react.shared-subset.production.min.js  
npm notice 190B    index.js                                   
npm notice 222B    jsx-dev-runtime.js                         
npm notice 214B    jsx-runtime.js                             
npm notice 999B    package.json                               
npm notice 218B    react.shared-subset.js                     
npm notice 109.9kB umd/react.development.js                   
npm notice 10.7kB  umd/react.production.min.js                
npm notice 10.7kB  umd/react.profiling.min.js                 
npm notice === Tarball Details === 
npm notice name:          react                                   
npm notice version:       18.2.0                                  
npm notice filename:      react-18.2.0.tgz                        
npm notice package size:  81.2 kB                                 
npm notice unpacked size: 316.1 kB                                
npm notice shasum:        555bd98592883255fa00de14f1151a917b5d77d5
npm notice integrity:     sha512-/3IjMdb2L9QbB[...]zkxtmq6g09fGQ==
npm notice total files:   20                                      
npm notice 
react-18.2.0.tgz
```
-   [using `npm pack`](https://stackoverflow.com/questions/15035786/download-source-from-npm-without-installing-it#comment102975970_27929112)
-   [using `npm view`](https://stackoverflow.com/a/27929112/111890)
    -   `.tgz`의 URL을 얻을 수 있다
---
[[tags/NodeJS]]