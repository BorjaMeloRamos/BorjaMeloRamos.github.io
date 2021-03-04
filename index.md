#  Tarea para AW03 Markdow

## Borja Melo Ramos
Formatear un texto **puede** ser entretenido si prestas atención a *los videos de clase*.

<p>En Visual Studio Code, es más sencillo</p>

<ol>
  <li>Introducir un título.</li>
  <li>Hacer una lista númerada.</li>
  <li>Introducir una cita, como la que añado más abajo.</li>
  <li>Un enlace a una página web.</li>
  <li>Introducir una parte de código.</li>
  <li>Subir una imagen.</li>
  
</ol>

<p><a href="https://burela.org/gl">Pagina WEB principal de mi pueblo, Burela.</a> </p>


<p>Para introducir una cita con enlace:</p>
<blockquote>
  <p>Buscamos una noticia de interes y de actualidad.
  
  "Todos contra China en inteligencia artificial: la Comisión de Seguridad Nacional de EEUU pide una alianza con la UE para hacerles frente". </p>
  <footer>
    <cite><a href="https://www.xataka.com/pro/todos-china-inteligencia-artificial-comision-seguridad-nacional-eeuu-pide-alianza-ue-para-hacerles-frente">NOTICIA PABLO RODRÍGUEZ @Pabrodri -Xakata-
 </a></cite>
  </footer>
</blockquote>

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    Mi pagina de prueba
  </head>
  <body>
    <img src="https://emeradiofm.com/wp-content/uploads/2019/11/burela.jpg" alt="Mi imagen de prueba">
  </body>
</html>



**EJEMPLO DE CODIGO** Cliente http para hacer peticiones a servicios externos. En Typescrip

export class HttpClient {
    private readonly circuitBreaker: CircuitBreakerProxy;

    constructor() {
        const breakDuration = TimeSpansInMilliSeconds.oneMinute;
        const maxFailedCalls = 5;
        const logger = new NoLogger();
        const leakTimeSpanInMilliSeconds = TimeSpansInMilliSeconds.tenMinutes;
        this.circuitBreaker = new CircuitBreakerProxy(breakDuration, maxFailedCalls, leakTimeSpanInMilliSeconds, logger);
    }

    // eslint-disable-next-line @typescript-eslint/no-explicit-any
    async post<T>(url: string, data?: any, options?: HttpClientOptions): Promise<HttpResponse<T>> {
        const postRequest = async (): Promise<HttpResponse<T>> => axios.post(url, data, options);
        return this.circuitBreaker.execute(postRequest, Guid.createEmpty());
    }

    async get<T>(url: string, options?: HttpClientOptions): Promise<HttpResponse<T>> {
        const getRequest = async (): Promise<HttpResponse<T>> => axios.get(url, options);
        return this.circuitBreaker.execute(getRequest, Guid.createEmpty());
    }
}
