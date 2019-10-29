# app-ms-ole-db-sql-driver-18.2.2
Microsoft OLE DB Driver for SQL Server

Howto
----------------
1. Add variable {{ def_ans_repo }} to your group_vars or change it in your playbook or role.
2. Zip all files in 1 file.
3. Upload the file to the web/download server.
4. Edit defaults/main.yml to your needs.
5. Add the role to your playbook.

Example Playbook
----------------

This is an basic example, how to use the role:

    - hosts: windows_computers

      vars:

      roles:
        - app-ms-ole-db-sql-driver-18.2.2



This is an example how to use the role with custom variable(s):

    - hosts: windows_computers
      become: true

      vars:
        # -- custom settings - app-ms-ole-db-sql-driver-18.2.2 --
        pkg_arguments: 'IACCEPTMSOLEDBSQLLICENSETERMS=YES ADDLOCAL=ALL'

      roles:
        - app-ms-ole-db-sql-driver-18.2.2

Source(s)
----------------
* https://docs.microsoft.com/en-us/sql/connect/oledb/applications/installing-oledb-driver-for-sql-server?view=sql-server-ver15