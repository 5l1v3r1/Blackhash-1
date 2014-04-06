Common Blackhash Usage

1. Sys admin creates a filter from his system hashes then sends the filter to
   password auditor.

      bh system_nt_hashes.txt system_nt.filter create

2. Password auditor tests known weak hashes against the filter.

      bh top_100_nt_hashes.txt system_nt.filter test > weak_hashes.txt

3. Password auditor creates a weak filter then sends it back to the Sys admin.

      bh weak_hashes.txt weak.filter create

4. Sys admin uses weak filter to identify accounts with weak passwords.

      bh system_nt_hashes.txt weak.filter test

Notes

    This is just an example to demonstrate Blackhash usage. During an actual
audit, the password auditor would test many hashes against the filter, not just
a few.

