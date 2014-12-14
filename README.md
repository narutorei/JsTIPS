JsTIPS
======
## Where is JsTips ? ##

Is an open source project for creating a blog to disseminate knowledge in JavaScript developer community in not only english or portuguese, but in several.

## Features ##

##### Multi Language Posts #####

The main feature for all this to happen, each post may be translated into any other language, which will be identified from the user's browser, however, if a translation is not found, the application will suggest to the user to translate the post and appears this post in English (this feature is open to ideas!)

##To install

    npm install

##To run

    npm start

##To see running

    http://localhost:3000

##The API

> GET /api/beers

> GET /api/beers/populate

> GET /api/beers/\_id/:id

> POST /api/beers/

> PUT /api/beers/\_id/:id

> DELETE /api/beers/\_id/:id


#Directory Layout
    back/
      bin/
      config/
        db.js
      modules/
        main/
        expose/
        {{entity}}/
          api/
            controller.js
            routes.js
          views/
            create.jade
            edit.jade
            list.jade
            remove.jade
            show.jade
          controller.js
          model.js
          routes.js

    front/
      bower_components/
      css/
      js/
        lib/
        modules/
          {{entity}}/
            controllers.js
            services.js
            directives.js
            filters.js


#Nomenclature
##AngularJs

###Angularjs - Modules
Name:
>{Entity}{Action}Controller

Folder:
>/public/js/modules/{{entity}}

###Angularjs - Controllers
Name:
>{Entity}{Action}Controller

Folder:
>/public/js/modules/{{entity}}/controllers.js

###Angularjs - Services
Name:
>{Entity}{Service|Factory}

Folder:
>/public/js/modules/{{entity}}/services.js

###Angularjs - Filters
Name:
>{Entity}{FilterName}

Folder:
>/public/js/modules/{{entity}}/services.js

###Angularjs - Directives
Name:
>{Entity}{DirectiveName}

Folder:
>/public/js/modules/{{entity}}/directives.js