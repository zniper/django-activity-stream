Django Activity Stream Documentation
==================================================

Django Activity Stream is a way of creating activities generated by the actions on your site.

It is designed for generating and displaying streams of interesting actions and can handle following and unfollowing of different activity sources.
For example, it could be used to emulate the Github dashboard in which a user sees changes to projects they are watching and the actions of users they are following.

Action events are categorized by four main components.

 * ``Actor``. The object that performed the activity.
 * ``Verb``. The verb phrase that identifies the action of the activity.
 * ``Action Object``. *(Optional)* The object linked to the action itself.
 * ``Target``. *(Optional)* The object to which the activity was performed.

``Actor``, ``Action Object`` and ``Target`` are `GenericForeignKeys <https://docs.djangoproject.com/en/dev/ref/contrib/contenttypes/#django.contrib.contenttypes.fields.GenericForeignKey>`_ to any arbitrary Django object and so can represent any Django model in your project.
An action is a description of an action that was performed (``Verb``) at some instant in time by some ``Actor`` on some optional ``Target`` that results in an ``Action Object`` getting created/updated/deleted.

For example: `justquick <https://github.com/justquick/>`_ ``(actor)`` *closed* ``(verb)`` `issue 2 <https://github.com/justquick/django-activity-stream/issues/2>`_ ``(object)`` on `django-activity-stream <https://github.com/justquick/django-activity-stream/>`_ ``(target)`` 12 hours ago

Nomenclature of this specification is based on the Activity Streams Spec: `<http://activitystrea.ms/>`_


Contents:

.. toctree::
   :maxdepth: 2
   :glob:

   installation
   configuration
   actions
   data
   follow
   streams
   templatetags
   feeds
   changelog
   api

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
