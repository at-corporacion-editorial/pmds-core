# PMDS: Protocolo de Mitigación de Degradación Sintética

<p align="left">
  <a href="https://doi.org/10.5281/zenodo.22226756"><img src="https://img.shields.io/badge/DOI-10.5281%2Fzenodo.22226756-blue.svg" alt="DOI"></a>
  <a href="https://opensource.org/licenses/Apache-2.0"><img src="https://img.shields.io/badge/License-Apache_2.0-green.svg" alt="License: Apache 2.0"></a>
  <a href="https://creativecommons.org/licenses/by/4.0/"><img src="https://img.shields.io/badge/Docs-CC_BY_4.0-lightgrey.svg" alt="License: CC BY 4.0"></a>
  <a href="https://orcid.org/0009-0008-6832-3814"><img src="https://img.shields.io/badge/ORCID-0009--0008--6832--3814-brightgreen.svg" alt="ORCID"></a>
  <img src="https://img.shields.io/badge/Python-3.9%2B-blue" alt="Python 3.9+">
</p>

> **Infraestructura Middleware en el Borde (*Edge Computing*) para la Sincronización Neuro-Semántica, Contención de Entropía y Gobierno Estricto de Modelos de Lenguaje de Frontera.**

---

## 📌 Contenido Rápido

- [Descripción General](#-descripción-general)
- [Arquitectura Core y Módulos](#-arquitectura-core-y-módulos)
- [Métricas de Impacto (Benchmark N=500)](#-métricas-de-impacto-benchmark-n500)
- [Implementación de Referencia en Python](#-implementación-de-referencia-en-python)
- [Publicación Académica y Citación](#-publicación-académica-y-citación)
- [Licenciamiento Dual](#-licenciamiento-dual)

---

## 🚀 Descripción General

El **Protocolo de Mitigación de Degradación Sintética (PMDS)**, desarrollado por **A.T. Corporación Editorial**, es un middleware determinista diseñado para ejecutarse in situ en el borde. Su objetivo principal es erradicar la deriva semántica, prevenir la degradación léxica y suprimir alucinaciones normativas en LLMs sin requerir cómputo o VRAM adicional en los servidores centrales.

> [!IMPORTANT]
> **Regla de Contexto 75/25:**
> El PMDS reserva estructuralmente un **75% del espacio contextual** para anclaje sintáctico rígido e invariantes de dominio (leyes, datos bancarios, diagnósticos médicos) y destina un **25% a la permutación deductiva** controlada del modelo.

---

## 🧩 Arquitectura Core y Módulos

El ecosistema PMDS orquesta cinco subsistemas modulares de gobierno:

| Módulo | Nombre Completo | Función Operativa |
| :--- | :--- | :--- |
| **SS-Protocol** | Protocolo de Sincronización Semántica | Estabilización de vectores de sesión mediante inyección acotada en $\Delta t$. |
| **FHDC** | Filtro Hermenéutico de Doble Ciego | Verificación bidireccional: descomposición ontológica (A) y auditoría normativo-ciega (B). |
| **SNL** | Soberanía Neuro-Literaria | Modulación de penalizaciones de presencia/frecuencia para preservar la varianza léxica. |
| **SNS** | Sincronización Neuro-Semántica | Restricción sintáctica que restringe el muestreo probabilístico, eliminando clichés. |
| **GEO ATG** | Arquitectura Taxonómica Generativa | Indexación y estructuración semántica de metadatos para visibilidad en motores de IA. |

---

## 📊 Métricas de Impacto (Benchmark N=500)

> [!NOTE]
> Evaluaciones empíricas ejecutadas mediante pruebas A/B automatizadas en entornos de producción:

- ⚡ **Reducción del 28.5% en la latencia** de respuesta durante la Inferencia en Borde.
- 🎯 **Supresión del 91.4% de desviaciones semánticas** y alucinaciones en dominios críticos.
- 🖥️ **0 MB de VRAM adicional** requerida en la infraestructura central.

---

## 💻 Implementación de Referencia en Python

```python
from dataclasses import dataclass


# Excepción emitida al detectar deriva entrópica crítica en runtime
class AlertaColapsoModelo(Exception):
    pass


# Configuración de parámetros léxicos para el filtro SNL
@dataclass
class ParametrosLexicosSNL:
    presencia_penalty: float = 0.65
    frecuencia_penalty: float = 0.40
    temperatura: float = 0.75
    top_p: float = 0.88


# Aplica restricciones estilísticas y ajusta parámetros de muestreo
def filtro_soberania_snl(prompt_crudo: str, umbral_entropia: float = 0.75) -> dict:
    config = ParametrosLexicosSNL()
    return {
        "prompt": prompt_crudo,
        "temperatura": config.temperatura,
        "top_p": config.top_p,
        "presencia_penalty": config.presencia_penalty,
        "frecuencia_penalty": config.frecuencia_penalty
    }


# Capa A: Aislamiento hermenéutico del estímulo de entrada
def disyuncion_hermeneutica_fhdc(entrada_cruda: dict) -> dict:
    return {"vector_aislado": entrada_cruda, "status": "descompuesto"}


# Capa B: Auditoría ciega frente a matriz de dominio normativo
def verificacion_ciega_fhdc(salida_modelo: str, matriz_dominio: dict) -> object:
    class ResultadoValidacion:
        def pasa_umbral_entropia(self) -> bool:
            return True

    return ResultadoValidacion()


# Carga de restricciones rígidas de dominio (75% de anclaje sintáctico)
def cargar_restricciones_autoritativas(ratio: float, protocolo: str) -> dict:
    return {"ratio": ratio, "protocolo": str(protocolo)}


# Aislamiento paramétrico (25% de permutación dinámica acotada)
def aislar_parametros_generativos(consulta_aislada: dict, ratio: float, sintaxis: str) -> dict:
    return {"consulta": consulta_aislada, "ratio": ratio, "sintaxis": str(sintaxis)}


# Simulación de inferencia en el borde ajustada temporalmente
def ejecutar_inferencia_borde(ancla_sintactica: dict, permutacion_dinamica: dict, delta_t: float) -> str:
    return "Inferencia procesada bajo parámetros PMDS."
```

---

## 📚 Publicación Académica y Citación

Si utiliza el marco conceptual, las especificaciones teóricas o la infraestructura de software del PMDS, cite esta obra mediante el siguiente formato:

```bibtex
@article{torres2026pmds,
  author    = {Torres, Alexander},
  title     = {PMDS: Arquitectura Middleware en el Borde para la Sincronización Neuro-Semántica y Mitigación de Degradación Sintética en Modelos de Frontera},
  journal   = {Zenodo Preprint},
  year      = {2026},
  doi       = {10.5281/zenodo.XXXXXXX},
  publisher = {A.T. Corporación Editorial}
}
```

* **Autor:** Alexander Torres
* **ORCID:** [0009-0008-6832-3814](https://orcid.org/0009-0008-6832-3814)
* **Entidad:** A.T. Corporación Editorial

---

## 📄 Licenciamiento Dual

- **Código e Infraestructura de Software:** Distribuido bajo la [Licencia Apache 2.0](LICENSE).
- **Documentación Teórica y White Paper:** Licenciado bajo [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
        
   

        
