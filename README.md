# Proyecto_Lenguajes_1 UNITEC

## Lenguajes de programación
### Elaborado por Eddas Carrasco, Jasser Ramos y Luis Enriquez

### Especificación
Crear la base de hechos con las siguientes listas:
aula(numero, num_escritorios, num_escritorios_izq).
Num_escritorios: el total de escritorios en la habitación
Num_escritorios_izq: el total de escritorios para izquierdos
estudiante(id, izq_der, lista_de_cursos)
fechaexam(id_curso, lista_de_fechas)

### Ejemplo de la base de datos:

aula(nh101, 50, 10).<br/>
aula(nh201, 50, 10).<br/>
aula(nh301, 50, 10).<br/>
aula(m2001, 30, 5).<br/>
aula(etaa2, 30, 5).<br/>
aula(etb101, 20, 5).<br/>
aula(hkd101, 80, 20).<br/>
estudiante(2000100001, 1, [math101, phys201, ec201]) .<br/>
estudiante(2000100002, 1, [math101, phys201, hist301]).<br/>
estudiante(2000100003, 1, [math101, ec201, hist301]) .<br/>
estudiante(2000100004, 1, [math101, phys201, ec201, hist301]) .<br/>
estudiante(2000100007, 0, [ec201, phys201]).<br/>
estudiante(2000100015, 0, [ec201, hist301]) .<br/>
estudiante(2000100016, 0, [cmpe150, hist301]).<br/>
estudiante(2000100017, 0, []).<br/>
estudiante(2000100008, 0, [math101, phys201]) .<br/>
estudiante(2000100009, 1, [phys201, ec201]).<br/>
estudiante(2000100010, 0, [cmpe150, math101]).<br/>
estudiante(2000100011, 0, [cmpe150, hist301).<br/>
estudiante(2000100012, 1, [math101, phys201]).<br/>
estudiante(2002100009, 0, [math101, ec201, hist301]).<br/>
estudiante(2002100071, 0, [phys201, ec201, hist301]).<br/>
estudiante(2002100053, 0, [cmpe150, ec201]).<br/>
estudiante(2002100040, 1, [math101, hist301]).<br/>
estudiante(2002100032, 0, [phys201, ec201]).<br/>
estudiante(2002100010, 0, [cmpe150]).<br/>
estudiante(2002103010, 1, []).<br/>
fechaexam(cmpe150, ['15.04.2018', '25.05.2018', '04.06.2018']).<br/>
fechaexam(math101, ['17.04.2018', '15.05.2018', '04.06.2018']).<br/>
fechaexam(phys201, ['15.04.2018', '19.05.2018', '05.06.2018']).<br/>
fechaexam(ec201, ['16.04.2018', '20.05.2018', '02.06.2018']).<br/>
fechaexam(hist301, ['14.04.2018', '21.05.2018', '01.06.2018']).<br/>

### Paso 1
Debe de crear por lo menos 200 hechos en total
### Paso 2
Programar los siguientes predicados
1. Implemente el predicado lista_estudiantes(id_curso, lista_e). Toma el id del curso y
agrega a lista_e los estudiantes que toman el curso.
 <br/><br/> lista_estudiantes(MATH101, L). L = [2000100001, 2000100002, 2000100003, 2000100004,
  2000100008, 2000100010, 2000100012, 2002100009, 2002100040]

2. Implemente el predicado lista_fechas(id_estudiante, lista_fechas)
Toma el id del estudiante y agrega a lista_fechas las fechas de los examenes de los
cursos que está tomando <br/> <br/>
lista_fechas(2000100017, D). D = []
lista_fechas(2002100010, D). D = ['15.04.2010', '25.05.2010', '04.06.2010']
lista_fechas(2000100007, D). D = ['16.04.2010', '20.05.2010','02.06.2010', '15.04.2010',
'19.05.2010', '05.06.2010']
lista_fechas(2000100004, D). D = ['17.04.2010', '15.05.2010', '04.06.2010', '15.04.2010',
'19.05.2010', '05.06.2010', '16.04.2010', '20.05.2010', '02.06.2010', '14.04.2010',
'21.05.2010', '01.06.2010']

3. Implemente el predicado aulas_adecuadas(id_curso, lista_aulas) que toma el id del
curso y agrega a lista_aulas, el código del aula que tiene la cantidad suficiente de
escritorios para izquierdos para ese curso.
<br/><br/>aulas_adecuadas(MATH101, S). S = [NH101, NH201, NH301, HKD101]
aulas_adecuadas (MATH301, S). S = []
aulas_adecuadas (CMPE150, S). S = [NH101, NH201, NH301, M2001, ETAA2, ETB101,
HKD101]
aulas_adecuadas (PHYS201, S). S = [NH101, NH201, NH301, M2001, ETAA2, ETB101,
HKD101]
