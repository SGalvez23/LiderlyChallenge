Se utilizó el objeto contact (renombrado como Student) para guardar la información del estudiante junto a su información necesaria para generar la cotización.
En el objeto Student se añadieron los campos personalizados: Calcu_Costo_Estado__c, Cantidad_Materias__c, Costo_Final__c, Descuento_Becas__c, Descuento_CantMaterias__c, Descuento_Contado__c, Descuento_Final__c, Descuentos__c, Estado__c, Forma_de_Pago__c, Matricula__c, Periodo__c y Promedio__c. Los campos para calcular descuentos son campos de fórmula, mientras que el resto son picklists y la matrícula es un número automático e único con la extensión “EST-”.

El cálculo de los costos se realiza con los campos de fórmula. Estos campos también realizan algunas de las validaciones como no pasar de más del 60% de descuento. Al agregar un nuevo estudiante el trigger genera la cotización en PDF para ser mandada por correo. La cotización muestra el nombre del alumno, el tipo de beca que tiene, el costo final a pagar y las fechas de pago.
Si la forma de pago es de contado, solo se muestra la fecha de pago de la inscripción. Si es en mensualidades se muestran las mensualidades a pagar cada día 10 del mes.
Ejemplo de dos cotizaciones, una con pago en mensualidades y otra de contado.