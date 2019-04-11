---
lang: en
title: 'Using components'
keywords: LoopBack 4.0, LoopBack 4
sidebar: lb4_sidebar
permalink: /doc/en/lb4/Using-components.html
---

Components can be add to your application using the `app.component()` method.
The following is an example of installing and using a component.

Install the following dependencies:

```sh
npm install --save @loopback/authentication
npm install @types/passport
```

Load the component in your application:

```ts
import {RestApplication} from '@loopback/rest';
import {AuthenticationComponent} from '@loopback/authentication';

const app = new RestApplication();
// Add component to Application, which provides bindings used to resolve
// authenticated requests in a Sequence.
app.component(AuthenticationComponent);
```
