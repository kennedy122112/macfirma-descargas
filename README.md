# MacFirma — descargas

Firmador local de documentos PDF para macOS. Produce firmas **PAdES** con certificados digitales instalados en el
**Llavero** de macOS, en un archivo **.pfx / .p12** o en el **DNIe** (con lector de tarjetas). Los documentos se firman
en tu Mac: nada se envía a ningún servidor.

> **Herramienta independiente y no oficial.** MacFirma no es un producto de la PCM, de Firma Perú, de RENIEC ni de
> Apple, ni cuenta con su respaldo, y no es un software de firma acreditado ante INDECOPI. Revisa el
> [aviso legal](#aviso-legal) antes de usarla.

## Descargar

| Tu Mac | Instalador |
|---|---|
| **Chip Apple** (M1, M2, M3, M4…) | [MacFirma-0.5-arm64.dmg](https://github.com/kennedy122112/macfirma-descargas/releases/latest/download/MacFirma-0.5-arm64.dmg) |
| **Intel** | [MacFirma-0.5-x86_64.dmg](https://github.com/kennedy122112/macfirma-descargas/releases/latest/download/MacFirma-0.5-x86_64.dmg) |

¿Cuál es tu Mac? Menú  › **Acerca de esta Mac**: «Chip» Apple → `arm64`; «Procesador» Intel → `x86_64`.

Todas las versiones están en [Releases](https://github.com/kennedy122112/macfirma-descargas/releases).

## Requisitos

- macOS 11 (Big Sur) o posterior.
- No necesitas instalar Java ni nada adicional: viene dentro de la aplicación.
- Tu propio certificado digital: instalado en el Llavero, en un archivo .pfx/.p12, o tu DNIe con un lector de tarjetas.

## Instalar

1. Abre el `.dmg` y arrastra **MacFirma** a **Aplicaciones**.
2. Abre MacFirma. La primera vez macOS la bloquea porque no está notarizada por Apple: cierra el aviso.
3. Ve a **Ajustes del Sistema › Privacidad y seguridad**, baja hasta el mensaje sobre MacFirma y pulsa
   **«Abrir igualmente»**. Desde entonces se abre normalmente.

Si macOS dice que **«MacFirma está dañada»**, no lo está: es la marca de cuarentena de los archivos descargados.
Quítala en Terminal y vuelve a abrirla:

```bash
xattr -dr com.apple.quarantine /Applications/MacFirma.app
```

La primera vez que firmes con un certificado del Llavero, macOS pedirá permiso para usar su clave: elige
**«Permitir siempre»**.

## Verificar la descarga (opcional)

```bash
shasum -a 256 ~/Downloads/MacFirma-0.5-*.dmg
```

| Archivo | SHA-256 |
|---|---|
| MacFirma-0.5-arm64.dmg | `0febe8d02308cda9cda2e5f4f87de8d69d9024c235bf4ea63b26912b666494ed` |
| MacFirma-0.5-x86_64.dmg | `f6295baaf541e34a480eae996f83fecbdbe2bd9c2e46b95918b68617484e47a6` |

## Privacidad

MacFirma funciona sin conexión a servidores propios: no recopila, almacena ni envía datos personales, documentos,
certificados ni PIN. Las contraseñas y el PIN se escriben solo en la aplicación y no se guardan.

## Aviso legal

- MacFirma se entrega **gratuitamente y «tal cual»**, sin garantías de ningún tipo, expresas o implícitas. El autor no
  es responsable de daños, pérdidas o rechazos derivados de su uso.
- Es una herramienta **independiente y no oficial**. No es un software de firma digital acreditado ante INDECOPI ni
  forma parte de la Infraestructura Oficial de Firma Electrónica (IOFE). Las marcas y nombres de terceros se mencionan
  solo para describir compatibilidad.
- Cada usuario es responsable de los documentos que firma y del uso de su certificado. **Verifica tus documentos
  firmados** en el validador oficial antes de presentarlos; si una entidad exige un software de firma determinado,
  usa el que ella indique.
- Se prohíbe redistribuir versiones modificadas presentándolas como MacFirma.

MacFirma incluye componentes de código abierto de terceros: ver [LICENCIAS-DE-TERCEROS.md](LICENCIAS-DE-TERCEROS.md).

© 2026 Brian Steve Kennedy Meneses Morales.
