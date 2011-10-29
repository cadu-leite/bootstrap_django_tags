===========================
bootstrap_django_tags Pluggable App
===========================

bootstrap_django_tags is a Django pluggable application to generate forms or form_fields html tags to use with Bootstrap from Twitter (http://twitter.github.com/bootstrap/)

Installation  
=============================
 
Copy the "bootstrap.css"  file to the media server path (static) directory of you project.
::
  
  INSTALLED_APPS = (
      ...

      'bootstrap_tags',

  )


to use the tags in django tamplates 
::

  {% load bootstrap_tags %}

 <form method="POST">
  {% csrf_token %}
  <fieldset>
   {% bootstrap_form_field form %}
  </fieldset>
  <div class="actions" >
   <input type="submit" class="btn primary" value="Enviar">
   <input type="reset" class="btn " value="Cancelar">
  </div>
 </form>

you may use the same template tag to format fields, not the entire form

::

 <form method="POST">
  {% csrf_token %}
  <fieldset>
	  {% bootstrap_form_field form.username %}
   {% bootstrap_form_field form.password %}
	 </fieldset>
	 <div class="actions" >
	  <input type="submit" class="btn primary" value="Enviar">
	  <input type="reset" class="btn " value="Cancelar">
	 </div>
 </form>


AUTHORS
=======
bootstrap_django_tags created by ZNC Sistemas  (http://www.znc.com.br/)

Contributors:

 * Carlos Leite
 * Denis Costa
 * Luiz Vital