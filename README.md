Passos para atualização:

1. Fez o backup pela interface:
/var/opt/f-secure/fspms/data/backup/2020_11_24_15_27_15_sdata.backup.zip

2. Novo deb:

https://download.f-secure.com/corpro/pm_linux/pm_linux15.10/fspms_15.10.94031_amd64.deb

3. Tipo uma "migration" pós instalação:

./fspms-db-maintenance-tool

4. SUbir o serviço
/etc/init.d/fspms start

Instalação iterativa zerara pós rodar .deb:

  /opt/f-secure/fspms/bin/fspms-config


    #- name: Executa configuração
    #  shell: "/opt/f-secure/fspms/bin/fspms-config"

  #- name: Procedimento de restauração de backups
  #  copy:
  #    src: /home/acesarfs/projetos/provisioner/roles/fflch.f-secure/templates/fspms.h2.db
  #    dest: /var/opt/f-secure/fspms/data/h2dv/fspms.h2.db
  #    owner: fspms
  #    group: fspms
  #    mode: 0644
  #  tags:
  #    - fspms.h2.db

