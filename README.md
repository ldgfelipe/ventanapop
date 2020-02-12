# ventanapop

Simple ventana pop up configurable 
utiliza bootstrap 
para modal- alertas u otro tipo de eventos para mostrar en ventana 

props
  <ventanapop 
  
  bgcolor="#fff"  //*- #fff or white -*/
  opacity="0.5"  //*- 0.1 a 1 -*/
  @cierrapop="ventana=$event" //*- ventana o la variable declarada en v-if para cerrar -- *//
  v-if="ventana===true"
  
  ></ventanapop>
