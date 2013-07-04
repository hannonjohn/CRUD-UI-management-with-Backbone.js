CRUD UI management with Backbone.js
===================================

This repo contains JS templates for the management of CRUD UI’s with Backbone.js.

The methodology is optimised to use as little memory as possible, and is layed out in a clear and simple way.

I've annotated the source.

Controller.js is responsible for a ListView, the ItemViews, and the creation of a single EditView 
instance whose el is moved around the DOM as needed.

The EditView is responsible for adding and editing, i.e. the "edit-mode" UI. It holds a clone of the item models used 
in the Controller. It is this view which is doing the saves and deletions back to the server (Backbone.sync).

The EditView will fire 3 callbacks to the Controller - options.saved(id), options.deleted(id), options.cancelled(id).
