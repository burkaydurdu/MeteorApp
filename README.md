# Meteor File Structure

```
 client/
  main.js
  main.html
  main.css
 imports/
  api/
    users/
      methods.js
      users.js
    ...
  startup/
    both/
      index.js
    client/
      index.js
      routes.js
      utils.js
    server/
      index.js
      publications.js
  ui/
    components/
      footer/
        index.js
        index.html
      navbar/
      sidenav/
      ...
    layouts/
      index.js
      index.html
    pages/
      login/
        index.js
        index.html
      ...
 public/
  logo/
  image/
 server/
  main.js
```

**server**
```
import '/imports/startup/server/'
import '/imports/startup/both/'
```
**client**
```
import '/imports/startup/client'
import '/imports/startup/both'
```
**imports/both**
```
import '/imports/api/users/collectionName.js'
```
**imports/client**
```
//layouts
import '/imports/ui/layouts/'
//components
import '/imports/ui/components/navbar/'
import '/imports/ui/components/sidenav/'
import '/imports/ui/components/footer/'
//pages
import '/imports/ui/pages/login/'
//router
import './routes.js'
//global
import './utils.js'
```
**imports/server**
```
import '/imports/api/collectionName/methods.js'

import './publications.js'
```
