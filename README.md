Passos para atualização:

  1. Fez o backup pela interface:
  
    /var/opt/f-secure/fspms/data/backup/2020_11_24_15_27_15_sdata.backup.zip

  2. Após rodar o playbook com a instalação limpa, rorar tipo uma "migration" pós instalação:

    ./fspms-db-maintenance-tool

  3. SUbir o serviço

    /etc/init.d/fspms start

  4. Instalação iterativa zerara pós rodar o playbook (ou seja rodar o .deb):

    /opt/f-secure/fspms/bin/fspms-config

  5. Redirecionamentos na internuvem:

  - 47124 (pública) -> 8081 (f-secure)
  - 47123 (pública) -> 8080 (f-secure)
  - 47122 (pública) -> 443 (f-secure)
  - 47121 (pública) -> 80 (f-secure)


