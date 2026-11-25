# Solardrone · Comprobador de vuelos

Revisa una carpeta de vuelo **en tu ordenador y sin internet** antes de subirla a Argos.
Te dice lo mismo que la página de subida de Argos: cobertura del plano, mesas sin cubrir,
térmicas sin datos, fotos rotas, altura fuera de rango, saltos y tramos raros de la
trayectoria, fotos sin pareja, huecos en la numeración, carpetas atípicas o solapadas,
fotos antiguas, pausas largas y carpetas lejos de la planta.

Las fotos no salen de tu ordenador. La app solo se conecta para buscar actualizaciones;
si no hay conexión, funciona igual.

## Descargar

En **[Releases](../../releases/latest)**, el fichero de tu sistema:

| Sistema | Fichero |
|---|---|
| Windows 10/11 | `Solardrone-Comprobador-X.Y.Z-Windows.exe` |
| Mac (Apple Silicon o Intel) | `Solardrone-Comprobador-X.Y.Z-Mac-arm64.dmg` o `-x64.dmg` |
| Linux | `…-Linux-x86_64.AppImage` o `…-Linux-amd64.deb` |

## Instalar

**Windows.** Abre el `.exe`. Como el instalador aún no está firmado, Windows puede
enseñar «Windows protegió su PC»: pulsa **Más información → Ejecutar de todas formas**.
Se instala solo para tu usuario (no pide administrador) y deja un acceso en el escritorio.

**Mac.** Abre el `.dmg` y arrastra la app a Aplicaciones. Como aún no está firmada por
Apple, la primera vez: **clic derecho sobre la app → Abrir → Abrir**. En Mac la app
**no se actualiza sola**: te avisa de que hay versión nueva y la descargas de aquí.

**Linux.** `sudo apt install ./Solardrone-Comprobador-…-amd64.deb`, o da permiso de
ejecución al `.AppImage` y ábrelo.

## Usar

1. Elige el **tipo de inspección** (termografía, visual…).
2. Si tienes el plano de la planta (GeoJSON o KML), pulsa **Cargar plano…**: sin plano no
   se comprueba la cobertura por mesa ni la distancia a la planta.
3. Arrastra la carpeta del vuelo (o varias).
4. Arriba sale el veredicto: **verde** vuelo correcto, **ámbar** revisa los avisos,
   **rojo** hay que volver a volar o resubir.

## Actualizaciones

En Windows y Linux (AppImage) la app busca versión nueva al abrirse, la descarga y te
ofrece **Reiniciar y actualizar**. Sin conexión dice «No se pudo comprobar» y sigue
funcionando. La versión que tienes está arriba a la izquierda y en *Ayuda → Acerca de*.

## Si algo falla

Pulsa **Informe para soporte** (arriba a la derecha) y guarda el fichero `.json`.
Lleva la versión, el sistema, el resultado de la última revisión (solo resultados y
nombres de fichero, **nunca fotos**) y el registro de la app. Mándalo a
soporte@solardrone.es contando qué pasó.

| Síntoma | Qué hacer |
|---|---|
| Windows no deja instalar | «Más información → Ejecutar de todas formas» (instalador sin firmar). |
| Mac dice que la app está dañada o no se puede abrir | Clic derecho → Abrir. Si insiste: `xattr -dr com.apple.quarantine "/Applications/Solardrone Comprobador de vuelos.app"` |
| Una carpeta sale sin fotos | Ruta demasiado larga en Windows: mueve la carpeta a `C:\vuelos\` y vuelve a soltarla. |
| No sale la cobertura del plano | El plano no tiene paneles ni mesas, o no lo has cargado. |
| «No se pudo comprobar» en actualizaciones | Sin conexión o red de empresa que lo bloquea. La revisión no se ve afectada. |
