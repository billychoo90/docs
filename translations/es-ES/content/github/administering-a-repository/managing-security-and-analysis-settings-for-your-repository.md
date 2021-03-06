---
title: Administrar la configuración de seguridad y análisis para tu repositorio
intro: 'Puedes controlar las características que dan seguridad y analizan tu código en tu proyecto dentro de {% data variables.product.prodname_dotcom %}.'
permissions: Las personas con permisos administrativos en un repositorio pueden gestionar la configuración de análisis y seguridad del mismo.
redirect_from:
  - /articles/managing-alerts-for-vulnerable-dependencies-in-your-organization-s-repositories/
  - /articles/managing-alerts-for-vulnerable-dependencies-in-your-organizations-repositories/
  - /articles/managing-alerts-for-vulnerable-dependencies-in-your-organization
  - /github/managing-security-vulnerabilities/managing-alerts-for-vulnerable-dependencies-in-your-organization
versions:
  free-pro-team: '*'
  enterprise-server: '>=3.0'
---

{% if currentVersion == "free-pro-team@latest" %}
### Enabling or disabling security and analysis features for public repositories

You can manage a subset of security and analysis features for public repositories. Other features are permanently enabled, including dependency graph and secret scanning.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.repositories.navigate-to-security-and-analysis %}
4. Debajo de "Configurar la seguridad y las características de análisis", a la derecha de la característica, da clic en **Inhabilitar** o **Habilitar**. !["Enable" or "Disable" button for "Configure security and analysis" features in a public repository](/assets/images/help/repository/security-and-analysis-disable-or-enable-dotcom-public.png)
{% endif %}

### Enabling or disabling security and analysis features{% if currentVersion == "free-pro-team@latest" %} for private repositories{% endif %}

You can manage the security and analysis features for your {% if currentVersion == "free-pro-team@latest" %}private or internal {% endif %}repository. If your organization or enterprise has a license for {% data variables.product.prodname_GH_advanced_security %} then extra options are available. {% data reusables.advanced-security.more-info-ghas %}

{% data reusables.security.security-and-analysis-features-enable-read-only %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.repositories.navigate-to-security-and-analysis %}
4. Debajo de "Configurar la seguridad y las características de análisis", a la derecha de la característica, da clic en **Inhabilitar** o **Habilitar**.
{% if currentVersion == "free-pro-team@latest" %}If "{% data variables.product.prodname_secret_scanning_caps %}" is not displayed, you may need to enable {% data variables.product.prodname_GH_advanced_security %} first.
  ![Botón de "Habilitar" o "Inhabilitar" para las características de "Configurar la seguridad y el análisis"](/assets/images/help/repository/security-and-analysis-disable-or-enable-dotcom-private.png)
  {% endif %}
  {% if enterpriseServerVersions contains currentVersion and currentVersion ver_gt "enterprise-server@2.22" %}
  ![Botón de "Habilitar" o "Inhabilitar" para las características de "Configurar la seguridad y el análisis"](/assets/images/help/repository/security-and-analysis-disable-or-enable-ghe.png)
  {% endif %}

### Otorgar acceso a las alertas de seguridad

Después de que habilitas las alertas del {% data variables.product.prodname_dependabot %} o del {% data variables.product.prodname_secret_scanning %} para un repositorio en una organización, los propietarios y administradores de repositorio de ésta podrán ver las alertas predeterminadamente. Puedes dar acceso a equipos y personas adicionales para las alertas de un repositorio.

{% note %}

Los propietarios de organización y administradores de repositorio solo pueden otorgar acceso para ver alertas de seguridad, tales como aquellas del {% data variables.product.prodname_dependabot %} y del {% data variables.product.prodname_secret_scanning %}, a las personas o equipos que tengan acceso de escritura en el repositorio.

{% endnote %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.repositories.navigate-to-security-and-analysis %}
4. Debajo de "Acceso a las alertas", en el campo de búsqueda, comienza a teclear el nombre de la persona o equipo que quieres encontrar y luego da clic en su nombre dentro de la lista de coincidencias.
   {% if currentVersion == "free-pro-team@latest" %}
   ![Campo de búsqueda para otorgar acceso a las alertas de seguridad a personas y equipos](/assets/images/help/repository/security-and-analysis-security-alerts-person-or-team-search.png)
   {% endif %}
   {% if enterpriseServerVersions contains currentVersion and currentVersion ver_gt "enterprise-server@2.22" %}
   ![Campo de búsqueda para otorgar acceso a las alertas de seguridad a personas y equipos](/assets/images/help/repository/security-and-analysis-security-alerts-person-or-team-search-ghe.png)
   {% endif %}
5. Haz clic en **Guardar cambios**. ![Botón de "Guardar cambios" para los cambios realizados a la configuración de alertas de seguridad](/assets/images/help/repository/security-and-analysis-security-alerts-save-changes.png)

### Eliminar el acceso a las alertas de seguridad

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.repositories.navigate-to-security-and-analysis %}
4. Under "Access to alerts", to the right of the person or team whose access you'd like to remove, click
{% octicon "x" aria-label="X symbol" %}.
   {% if currentVersion == "free-pro-team@latest" %}
   ![Botón "x" para eliminar el acceso de alguien a las alertas de seguridad para tu repositorio](/assets/images/help/repository/security-and-analysis-security-alerts-username-x.png)
   {% endif %}
   {% if enterpriseServerVersions contains currentVersion and currentVersion ver_gt "enterprise-server@2.22" %}
   ![Botón "x" para eliminar el acceso de alguien a las alertas de seguridad para tu repositorio](/assets/images/help/repository/security-and-analysis-security-alerts-username-x-ghe.png)
   {% endif %}

### Further reading

- [Acerca de asegurar tu repositorio](/github/administering-a-repository/about-securing-your-repository)"
- "[Administrar la seguridad y la configuración de análisis para tu organización](/github/setting-up-and-managing-organizations-and-teams/managing-security-and-analysis-settings-for-your-organization)"
