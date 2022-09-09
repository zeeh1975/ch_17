## **Backend Coderhouse - Desafío 17 - Clase 34: Desplegar nuestro proyecto en la nube**

**Consigna:**
Crear un proyecto en Heroku.com para subir el servidor que venimos realizando, reformando todo lo necesario para su correcto funcionamiento en la nube.
Subir el código a Heroku.com, sin olvidar incluir el archivo .gitignore para evitar subir los node_modules. Comprobar que el proyecto inicie de manera correcta en la nube. Verificar que en su ruta raíz se encuentre la página pública del servidor.
El servidor debe seguir funcionando en forma local.
Realizar un cambio a elección en alguna vista, probar en forma local y subir nuevamente el proyecto a Heroku, verificando que la nueva reforma esté disponible online.
Revisar a través de una consola local, los mensajes enviados por nuestro servidor en Heroku a su propia consola.

**Resolucion del desafio:**

URL de la entrega desplegada en [Heroku](https://ch-desafio17.herokuapp.com/)

Comando para ver log de forma local: `heroku logs`

Output del comando:
```
2022-09-07T14:05:11.137918+00:00 heroku[web.1]: State changed from crashed to starting
2022-09-07T14:05:16.998788+00:00 heroku[web.1]: Starting process with command `npm start`
2022-09-07T14:05:18.828646+00:00 app[api]: Set SESSION_SECRET config vars by user eehernandez@gmail.com
2022-09-07T14:05:18.828646+00:00 app[api]: Release v7 created by user eehernandez@gmail.com
2022-09-07T14:05:19.738011+00:00 heroku[web.1]: Restarting
2022-09-07T14:05:20.890686+00:00 app[web.1]:
2022-09-07T14:05:20.890701+00:00 app[web.1]: > logger_gzip_performance@1.0.0 start
2022-09-07T14:05:20.890702+00:00 app[web.1]: > node src/server.js
2022-09-07T14:05:20.890702+00:00 app[web.1]:
2022-09-07T14:05:23.614788+00:00 app[web.1]: 2022-09-07T14:05:23.2323 INFO Servidor fork escuchando en el puerto 19198
2022-09-07T14:05:24.972840+00:00 heroku[web.1]: Stopping all processes with SIGTERM
2022-09-07T14:05:25.269799+00:00 heroku[web.1]: Process exited with status 143
2022-09-07T14:05:25.862185+00:00 heroku[web.1]: Starting process with command `npm start`
2022-09-07T14:05:29.608193+00:00 app[web.1]:
2022-09-07T14:05:29.608207+00:00 app[web.1]: > logger_gzip_performance@1.0.0 start
2022-09-07T14:05:29.608208+00:00 app[web.1]: > node src/server.js
2022-09-07T14:05:29.608208+00:00 app[web.1]:
2022-09-07T14:05:33.787358+00:00 app[web.1]: 2022-09-07T14:05:33.3333 INFO Servidor fork escuchando en el puerto 57443
2022-09-07T14:05:34.087790+00:00 heroku[web.1]: State changed from starting to up
2022-09-07T14:05:49.567283+00:00 app[api]: Release v8 created by user eehernandez@gmail.com
2022-09-07T14:05:49.567283+00:00 app[api]: Set SESSION_MAXAGE config vars by user eehernandez@gmail.com
2022-09-07T14:05:49.955548+00:00 heroku[web.1]: Restarting
2022-09-07T14:05:49.970929+00:00 heroku[web.1]: State changed from up to starting
2022-09-07T14:05:51.085699+00:00 heroku[web.1]: Stopping all processes with SIGTERM
2022-09-07T14:05:51.471017+00:00 heroku[web.1]: Process exited with status 143
2022-09-07T14:05:54.466017+00:00 heroku[web.1]: Starting process with command `npm start`
2022-09-07T14:05:56.334692+00:00 app[web.1]:
2022-09-07T14:05:56.334710+00:00 app[web.1]: > logger_gzip_performance@1.0.0 start
2022-09-07T14:05:56.334711+00:00 app[web.1]: > node src/server.js
2022-09-07T14:05:56.334711+00:00 app[web.1]:
2022-09-07T14:05:57.897275+00:00 app[web.1]: 2022-09-07T14:05:57.5757 INFO Servidor fork escuchando en el puerto 22493
2022-09-07T14:05:58.049990+00:00 heroku[web.1]: State changed from starting to up
2022-09-07T14:06:00.976412+00:00 app[web.1]: 2022-09-07T14:06:00.000 INFO GET /
2022-09-07T14:06:00.989243+00:00 heroku[router]: at=info method=GET path="/" host=ch-desafio17.herokuapp.com request_id=c94459b6-72b5-4a49-8a88-c826b8bc3706 fwd="190.18.99.187" dyno=web.1 connect=0ms service=17ms status=302 bytes=329 protocol=https
2022-09-07T14:06:01.180040+00:00 app[web.1]: 2022-09-07T14:06:01.011 INFO GET /login
2022-09-07T14:06:01.187943+00:00 heroku[router]: at=info method=GET path="/login" host=ch-desafio17.herokuapp.com request_id=9361add7-26f5-4345-8d69-6f16b2fd1502 fwd="190.18.99.187" dyno=web.1 connect=0ms service=7ms status=200 bytes=1280 protocol=https
2022-09-07T14:06:01.389902+00:00 app[web.1]: 2022-09-07T14:06:01.011 INFO GET /assets/styles/styles.css
2022-09-07T14:06:01.394715+00:00 heroku[router]: at=info method=GET path="/assets/styles/styles.css" host=ch-desafio17.herokuapp.com request_id=e444d1a4-be55-4e94-9060-80ae52277a85 fwd="190.18.99.187" dyno=web.1 connect=0ms service=3ms status=200 bytes=472 protocol=https
2022-09-07T14:06:01.591751+00:00 app[web.1]: 2022-09-07T14:06:01.011 INFO GET /assets/scripts/const.js
2022-09-07T14:06:01.596207+00:00 heroku[router]: at=info method=GET path="/assets/scripts/const.js" host=ch-desafio17.herokuapp.com request_id=e28f66dd-91f4-47c0-a596-92f15a70d873 fwd="190.18.99.187" dyno=web.1 connect=0ms service=3ms status=200 bytes=889 protocol=https
2022-09-07T14:06:01.787894+00:00 app[web.1]: 2022-09-07T14:06:01.011 INFO GET /assets/scripts/login.js
2022-09-07T14:06:01.792833+00:00 heroku[router]: at=info method=GET path="/assets/scripts/login.js" host=ch-desafio17.herokuapp.com request_id=e2778f19-b514-483c-a8d1-387330446ee3 fwd="190.18.99.187" dyno=web.1 connect=1ms service=4ms status=200 bytes=981 protocol=https
2022-09-07T14:06:01.984258+00:00 app[web.1]: 2022-09-07T14:06:01.011 INFO GET /favicon.ico
2022-09-07T14:06:01.990581+00:00 heroku[router]: at=info method=GET path="/favicon.ico" host=ch-desafio17.herokuapp.com request_id=e64eafb1-7a91-4d57-826d-07fb84cdd24e fwd="190.18.99.187" dyno=web.1 connect=0ms service=7ms status=200 bytes=3358 protocol=https
2022-09-07T14:06:11.010576+00:00 app[web.1]: 2022-09-07T14:06:11.1111 INFO POST /login
2022-09-07T14:06:11.139264+00:00 app[web.1]: 2022-09-07T14:06:11.1111 INFO Usuario no encontrado:
2022-09-07T14:06:11.280005+00:00 heroku[router]: at=info method=POST path="/login" host=ch-desafio17.herokuapp.com request_id=1bc20652-5291-4484-8790-f50c0e89201e fwd="190.18.99.187" dyno=web.1 connect=0ms service=296ms status=302 bytes=394 protocol=https
2022-09-07T14:06:11.582935+00:00 app[web.1]: 2022-09-07T14:06:11.1111 INFO GET /loginFailed
2022-09-07T14:06:11.711598+00:00 heroku[router]: at=info method=GET path="/loginFailed" host=ch-desafio17.herokuapp.com request_id=af366842-76ce-4bfa-9330-80c842eeef1e fwd="190.18.99.187" dyno=web.1 connect=0ms service=248ms status=401 bytes=510 protocol=https
2022-09-07T14:06:14.712779+00:00 app[web.1]: 2022-09-07T14:06:14.1414 INFO GET /signup
2022-09-07T14:06:14.840203+00:00 heroku[router]: at=info method=GET path="/signup" host=ch-desafio17.herokuapp.com request_id=b5622e52-0e0a-4bc6-9bfd-360b80995bd7 fwd="190.18.99.187" dyno=web.1 connect=0ms service=244ms status=200 bytes=1537 protocol=https
2022-09-07T14:06:15.141740+00:00 app[web.1]: 2022-09-07T14:06:15.1515 INFO GET /assets/scripts/const.js
2022-09-07T14:06:15.274333+00:00 heroku[router]: at=info method=GET path="/assets/scripts/const.js" host=ch-desafio17.herokuapp.com request_id=5aaf8e6d-ffb5-4756-b001-9542aeb487f5 fwd="190.18.99.187" dyno=web.1 connect=0ms service=250ms status=304 bytes=439 protocol=https
2022-09-07T14:06:15.568534+00:00 app[web.1]: 2022-09-07T14:06:15.1515 INFO GET /assets/scripts/signup.js
2022-09-07T14:06:15.694107+00:00 heroku[router]: at=info method=GET path="/assets/scripts/signup.js" host=ch-desafio17.herokuapp.com request_id=ddc37514-041b-4d4c-8a92-ad1d445dd0e9 fwd="190.18.99.187" dyno=web.1 connect=0ms service=243ms status=200 bytes=1237 protocol=https
2022-09-07T14:06:15.757144+00:00 app[web.1]: 2022-09-07T14:06:15.1515 INFO GET /assets/styles/styles.css
2022-09-07T14:06:15.885487+00:00 heroku[router]: at=info method=GET path="/assets/styles/styles.css" host=ch-desafio17.herokuapp.com request_id=40f564c8-5e90-4e42-bfbb-47ad5bc91af2 fwd="190.18.99.187" dyno=web.1 connect=0ms service=861ms status=304 bytes=438 protocol=https
2022-09-07T14:06:22.592828+00:00 app[web.1]: 2022-09-07T14:06:22.2222 INFO POST /signup
2022-09-07T14:06:23.406846+00:00 heroku[router]: at=info method=POST path="/signup" host=ch-desafio17.herokuapp.com request_id=76d7fb8b-7a29-42f8-bdca-0cbe9b265708 fwd="190.18.99.187" dyno=web.1 connect=0ms service=931ms status=302 bytes=381 protocol=https
2022-09-07T14:06:23.827061+00:00 app[web.1]: 2022-09-07T14:06:23.2323 INFO GET /
2022-09-07T14:06:23.953321+00:00 heroku[router]: at=info method=GET path="/" host=ch-desafio17.herokuapp.com request_id=04931906-79a4-46f5-9951-67362627601b fwd="190.18.99.187" dyno=web.1 connect=0ms service=360ms status=200 bytes=1774 protocol=https
2022-09-07T14:06:24.257515+00:00 app[web.1]: 2022-09-07T14:06:24.2424 INFO GET /
2022-09-07T14:06:24.382073+00:00 heroku[router]: at=info method=GET path="/" host=ch-desafio17.herokuapp.com request_id=2f6cf169-1454-4020-b9f8-2ecd855b2f36 fwd="190.18.99.187" dyno=web.1 connect=0ms service=360ms status=304 bytes=438 protocol=https
2022-09-07T14:06:24.591859+00:00 heroku[router]: at=info method=GET path="/socket.io/socket.io.js" host=ch-desafio17.herokuapp.com request_id=27ff35ac-097d-4a0f-a4f1-fdd5a94805e3 fwd="190.18.99.187" dyno=web.1 connect=0ms service=16ms status=200 bytes=26029 protocol=https
2022-09-07T14:06:24.809017+00:00 app[web.1]: 2022-09-07T14:06:24.2424 INFO GET /assets/styles/styles.css
2022-09-07T14:06:24.933642+00:00 heroku[router]: at=info method=GET path="/assets/styles/styles.css" host=ch-desafio17.herokuapp.com request_id=fe2bc668-db6d-4ecc-b69e-429395960202 fwd="190.18.99.187" dyno=web.1 connect=0ms service=359ms status=304 bytes=436 protocol=https
2022-09-07T14:06:25.206228+00:00 app[web.1]: 2022-09-07T14:06:25.2525 INFO GET /assets/scripts/const.js
2022-09-07T14:06:25.332652+00:00 heroku[router]: at=info method=GET path="/assets/scripts/const.js" host=ch-desafio17.herokuapp.com request_id=e1b1be4d-575c-4c6e-8eee-8ea787176bcc fwd="190.18.99.187" dyno=web.1 connect=0ms service=365ms status=304 bytes=437 protocol=https
2022-09-07T14:06:25.348463+00:00 app[web.1]: 2022-09-07T14:06:25.2525 INFO GET /assets/scripts/app.js
2022-09-07T14:06:25.473702+00:00 heroku[router]: at=info method=GET path="/assets/scripts/app.js" host=ch-desafio17.herokuapp.com request_id=389a0b8a-7bd3-43a3-bb22-d2cf7e4ca75d fwd="190.18.99.187" dyno=web.1 connect=0ms service=360ms status=200 bytes=2249 protocol=https
2022-09-07T14:06:25.650528+00:00 heroku[router]: at=info method=GET path="/socket.io/?EIO=4&transport=polling&t=OCOHWQY" host=ch-desafio17.herokuapp.com request_id=db7ebf79-4898-4daa-8f41-db2dd1cbc3da fwd="190.18.99.187" dyno=web.1 connect=0ms service=4ms status=200 bytes=255 protocol=https
2022-09-07T14:06:25.837667+00:00 heroku[router]: at=info method=POST path="/socket.io/?EIO=4&transport=polling&t=OCOHWTJ&sid=Xtxr7HaoHdL_b8T7AAAA" host=ch-desafio17.herokuapp.com request_id=e29c317f-d14e-4d6b-af21-9dc973d2f492 fwd="190.18.99.187" dyno=web.1 connect=0ms service=3ms status=200 bytes=121 protocol=https
2022-09-07T14:06:25.889058+00:00 app[web.1]: 2022-09-07T14:06:25.2525 INFO GET /user
2022-09-07T14:06:26.018991+00:00 heroku[router]: at=info method=GET path="/socket.io/?EIO=4&transport=polling&t=OCOHWTK&sid=Xtxr7HaoHdL_b8T7AAAA" host=ch-desafio17.herokuapp.com request_id=ab9f1922-99f1-4ad3-849e-bfced9c3196d fwd="190.18.99.187" dyno=web.1 connect=0ms service=1ms status=200 bytes=732 protocol=https
2022-09-07T14:06:26.133241+00:00 heroku[router]: at=info method=GET path="/user" host=ch-desafio17.herokuapp.com request_id=e1bb6e57-2928-40ab-ab50-060dbc6bce14 fwd="190.18.99.187" dyno=web.1 connect=0ms service=478ms status=200 bytes=470 protocol=https
2022-09-07T14:06:26.200293+00:00 heroku[router]: at=info method=GET path="/socket.io/?EIO=4&transport=polling&t=OCOHWZ3&sid=Xtxr7HaoHdL_b8T7AAAA" host=ch-desafio17.herokuapp.com request_id=98be675a-58db-46e4-b2cf-95db7d98b966 fwd="190.18.99.187" dyno=web.1 connect=0ms service=1ms status=200 bytes=922 protocol=https
2022-09-07T14:06:26.433338+00:00 app[web.1]: 2022-09-07T14:06:26.2626 INFO GET /assets/views/tabla_productos.hbs
2022-09-07T14:06:26.476767+00:00 heroku[router]: at=info method=GET path="/socket.io/?EIO=4&transport=polling&t=OCOHWc1&sid=Xtxr7HaoHdL_b8T7AAAA" host=ch-desafio17.herokuapp.com request_id=7c9a699d-3715-4d65-993e-8c434e453c1a fwd="190.18.99.187" dyno=web.1 connect=0ms service=88ms status=200 bytes=136 protocol=https
2022-09-07T14:06:26.558003+00:00 heroku[router]: at=info method=GET path="/assets/views/tabla_productos.hbs" host=ch-desafio17.herokuapp.com request_id=ff000970-99d4-4d51-8eed-97f017411341 fwd="190.18.99.187" dyno=web.1 connect=0ms service=360ms status=200 bytes=869 protocol=https
2022-09-07T14:06:26.618972+00:00 app[web.1]: 2022-09-07T14:06:26.2626 INFO GET /assets/views/tabla_chat.hbs
2022-09-07T14:06:26.744171+00:00 heroku[router]: at=info method=GET path="/assets/views/tabla_chat.hbs" host=ch-desafio17.herokuapp.com request_id=fb8c1640-8439-4d1d-a027-728c6f5bdb0c fwd="190.18.99.187" dyno=web.1 connect=0ms service=361ms status=200 bytes=737 protocol=https
2022-09-07T14:06:35.686265+00:00 heroku[router]: at=info method=GET path="/socket.io/?EIO=4&transport=websocket&sid=Xtxr7HaoHdL_b8T7AAAA" host=ch-desafio17.herokuapp.com request_id=f87c9bfb-ebd7-4993-8e33-c3e65b375d17 fwd="190.18.99.187" dyno=web.1 connect=0ms service=9498ms status=101 bytes=129 protocol=https
2022-09-07T14:06:35.929948+00:00 app[web.1]: 2022-09-07T14:06:35.3535 INFO GET /logout
2022-09-07T14:06:36.304961+00:00 heroku[router]: at=info method=GET path="/logout" host=ch-desafio17.herokuapp.com request_id=eb37dc09-87c8-43ba-9949-3a61ba9d1ffc fwd="190.18.99.187" dyno=web.1 connect=0ms service=611ms status=200 bytes=933 protocol=https
2022-09-07T14:06:36.606266+00:00 app[web.1]: 2022-09-07T14:06:36.3636 INFO GET /assets/styles/styles.css
2022-09-07T14:06:36.738623+00:00 heroku[router]: at=info method=GET path="/assets/styles/styles.css" host=ch-desafio17.herokuapp.com request_id=eec105d0-dc10-4dbf-9659-c178ca34560a fwd="190.18.99.187" dyno=web.1 connect=0ms service=251ms status=304 bytes=438 protocol=https
2022-09-07T14:06:39.059236+00:00 app[web.1]: 2022-09-07T14:06:39.3939 INFO GET /logout
2022-09-07T14:06:39.185676+00:00 heroku[router]: at=info method=GET path="/logout" host=ch-desafio17.herokuapp.com request_id=487f5bdd-1fa8-44c4-8a95-9b5c5a389042 fwd="190.18.99.187" dyno=web.1 connect=0ms service=243ms status=302 bytes=474 protocol=https
2022-09-07T14:06:39.367226+00:00 app[web.1]: 2022-09-07T14:06:39.3939 INFO GET /
2022-09-07T14:06:39.495945+00:00 heroku[router]: at=info method=GET path="/" host=ch-desafio17.herokuapp.com request_id=3fec8320-1253-44e7-a60f-e1a3cb82e37f fwd="190.18.99.187" dyno=web.1 connect=0ms service=245ms status=302 bytes=484 protocol=https
2022-09-07T14:06:39.660370+00:00 app[web.1]: 2022-09-07T14:06:39.3939 INFO GET /login
2022-09-07T14:06:39.784261+00:00 heroku[router]: at=info method=GET path="/login" host=ch-desafio17.herokuapp.com request_id=5c794f6f-7efb-463e-aaab-3301cd23c248 fwd="190.18.99.187" dyno=web.1 connect=0ms service=240ms status=200 bytes=1435 protocol=https
2022-09-07T14:06:40.087186+00:00 app[web.1]: 2022-09-07T14:06:40.4040 INFO GET /assets/scripts/const.js
2022-09-07T14:06:40.088093+00:00 app[web.1]: 2022-09-07T14:06:40.4040 INFO GET /assets/styles/styles.css
2022-09-07T14:06:40.212204+00:00 heroku[router]: at=info method=GET path="/assets/scripts/const.js" host=ch-desafio17.herokuapp.com request_id=778c8b2d-e2ab-4d1d-98cb-4a3fb9f566ed fwd="190.18.99.187" dyno=web.1 connect=0ms service=245ms status=304 bytes=439 protocol=https
2022-09-07T14:06:40.212606+00:00 heroku[router]: at=info method=GET path="/assets/styles/styles.css" host=ch-desafio17.herokuapp.com request_id=9ff56974-4d3b-4ed2-b397-4c058af3a8a3 fwd="190.18.99.187" dyno=web.1 connect=0ms service=245ms status=304 bytes=438 protocol=https
2022-09-07T14:06:40.503825+00:00 app[web.1]: 2022-09-07T14:06:40.4040 INFO GET /assets/scripts/login.js
2022-09-07T14:06:40.628724+00:00 heroku[router]: at=info method=GET path="/assets/scripts/login.js" host=ch-desafio17.herokuapp.com request_id=8d1fdc0c-5494-42c5-88bd-a4c59ca0f5ae fwd="190.18.99.187" dyno=web.1 connect=0ms service=243ms status=304 bytes=439 protocol=https
2022-09-07T14:06:40.924374+00:00 app[web.1]: 2022-09-07T14:06:40.4040 INFO GET /favicon.ico
2022-09-07T14:06:41.047877+00:00 heroku[router]: at=info method=GET path="/favicon.ico" host=ch-desafio17.herokuapp.com request_id=e07c0bdd-0f40-49a5-a991-bd85673f9c57 fwd="190.18.99.187" dyno=web.1 connect=0ms service=241ms status=304 bytes=440 protocol=https
```
