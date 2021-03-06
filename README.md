Client-side storage can be used to store data that is useful for the user (as an example, when an user login in a website and he does not have to do it when he come back).

There are a few options on Client-side storage, as an example we have:

- ### Web Storage
  Domain specific strategy that maintains a website information in a key/value structure. The values must be primitive values valid on JavaScript (Strings, numbers, booleans etc).
    - localStorage: stores the data until it's deleted. Suggested when you want to persist not privacy data about the user (for example, preferences on a website);
  
    - sessionStorage: stores the data while the user do not close his browser. Suggested when you want to persist information during user session (for example, you can store the uncompleted content of a post on a blog). Once the browser is close, the data is gone.

- ### IndexedDB
  A full Database that can be used to store data in the browser, but it must be used carefully to not overload user's browser.

  It allows to store objexts, arrays, images, videos and structured data indexed by a key.

  It's async, to not interfer with the usage of the web page.

  Some limitations of IndexedDB are:
    - Can't sync with back-end server;
    - It can be deleted by browser cleanup policy;
    - Can't be used in browser private mode;
    - The browser defines the limit of the storage;

    There are a few options of wrappers for IndexedDB that provides some syntax sugar and allows to use some features in a easier way, some examples are:

    - LocalForage: https://localforage.github.io/localForage/
    - Dexie.js: http://dexie.org/
    - ZangoDB: https://erikolson186.github.io/zangodb/
    - JSStore: http://jsstore.net/
  
- ### Service Workers (offline)
- Cache API