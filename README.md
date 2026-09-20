# CA par client — François Mouhot (tableau de bord en ligne)

Page statique du tableau de bord CA (ISOSIGN / François MOUHOT), accessible depuis
un mobile avec **les identifiants du CRM SIGNALISE**.

- Authentification : Supabase Auth du projet CRMsignalise (mêmes comptes que le CRM).
- Autorisation : colonne `ca_access` de la table `veille_roles`, gérée depuis la
  **gestion des utilisateurs du CRM**. Sans ce droit, la page n'affiche aucun chiffre.
- Données : publiées automatiquement depuis le PC du bureau à chaque `ACTUALISER.bat`
  (dossier `CRMPOOL\CA_MOUHOT_REFRESH`), dans la table `ca_dashboard_data` protégée par RLS.

Ce dépôt ne contient **aucun chiffre d'affaires et aucun secret** : uniquement l'écran de
connexion, le code de rendu, et la clé publique (« publishable ») Supabase, prévue pour être
publique et sans pouvoir propre — tout accès aux données passe par un compte autorisé.
