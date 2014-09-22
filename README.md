# InnoHub Ansible : deployer [![Build Status](https://travis-ci.org/innohub-ansible/deployer.svg?branch=master)](https://travis-ci.org/innohub-ansible/deployer)
=========

* Creates a deployer user
* Creates services directory
* Sets up SSH authorized keys

Role Variables
--------------

deployer_authorized_keys : Required : Adds the keys to the ~/.ssh/authorized_keys file

    deployer_authorized_keys:
      - ssh-rsa theactualkeyshouldbehere user@example.com

deployer_ssh_private_key : Required : Sets the deployer's private key

    deployer_ssh_private_key: |+
      -----BEGIN RSA PRIVATE KEY-----
      MIIEpAIBAAKCAQEAvbtseP1SZMsWiqVcpVTyC3F9EcIjlbD18bF18cllXs7KpN90
      2DtL+BLkZhJvGevdImjO142cp4ZOtZFf7uLTubVFBRYjATDO5UQQaNl8QaJPK1/N
      bDyJY3qq1WgCb0Z260P6Kq2XuAyCQ/dVbfvpIwqPxBwNeNLqzwLyD7OHkEi7e4UT
      v8GAdqrhON/clTsT6ZHVPfIz2H2ETIYEuMgxtwTKfsAaqpb1jvBUn1iUMXslf1B8
      aEO5tXY7GFA6kDd145dUveWR/RG961qJwL0BAr8d2g431FbMojBRQdMG+wVjrlvJ
      AKABSrwZmfmLrZLRTvkNaZQbdmQv/e9/AtcJRQIDAQABAoIBAQCB7GxVVbMsTl37
      R01v8gFlkKuCk5zmjq18enc3wR/nklf2GwbaY5CcKeO5efoWmAtv2rF5rgGOPkx7
      zTcSUMWHr/e5ifUihZfIK5nJEtUh5NGt9AapjbLPKlr9lCHGrUwVwxD2VLVGVVqG
      zEH19MErO7pDIqqfCF++rlewJNI6HEOk98JHZLFlj0f9LrSflUEXV5BS6748BiEi
      ZCiWoIv64gVqPFN+SipO5+2EGYKgO0jCiQ3goqs9srPBpgyvIwYA09gv8rGwY2Sl
      MHOcdEDCzzvalW1Y6CMEtx0bkerbYNKwlHb4RYZA0FeeJOuB/lFjXjsScTKxRfLv
      chWCn3/pAoGBAPwWvS+LSBYNLZY5fp0bUsQLkapiT5vSUmsAtSg2eCHWR9uNIEq0
      dCIXdVmWFkYMUtVT6wciN5xNujC0ElDSIlleWDCI5oXJqSTdGAoVfzGA5fdiRH36
      kxTCtGg/oexpMmsdug7MYkZATM5ZXke17VtVV0y5kiUw00jp0MFVeVLHAoGBAMCt
      A0RCfXMpPj1WtaaTNnJFv2napGa3jILbo1iwNwQ1xGGuBIqXz4/XWK8CJUEp275g
      8D4gLb+ZyOyUIBPPoXdbg7O0+WEtmGrTBP1jQNaexPP8RR96Pgr4Gm9pIHHT00dS
      m4Ayr82lfLJcixnxoosydfarcVDgg/PcG+IfvneTAoGBAJYKdrn4nYQ6fbqfJ+Qc
      oit7c0zFTPrCuTlk524y1VfWcViU6/Zq54BvE/KpaUJyDU9ZrlbFn/HRNZPNaeVe
      3QDyLW1d3k8dEyaUzb0axGTTgoy2mWueG7LMnJI75YWPq2mj/NzX+1oy5UQgXwQx
      nT+yUM6i2QB3yhnoyM55sEd7AoGADlsVujlGBZWWGJXkVPP1A5Ck0WtEAo88feeF
      hS8j+kFTT3/awMTM50fBSNDdG7zVrZqla8uT/QmlSdNDjJZUzoLYDkS2rAHssFDm
      t0Z050jPHeq278B47PJNbe2kSDbjMBY8ldGw/Z6N6vAwQQ+a78ojtexSNhd0XXAR
      98grtdcCgYBbJWNa7vga5OX3k+77tBdrxe6atiYqOcmbpVLW9/W/d/ihIrn+bjw5
      LJDWQUkKR0Utnf29cRotLjzNoVmFElYJ3k+IfmZ3U0bflnSxjf8HAxU9acIX+ewb
      5abu4AAD7EpaHc8Cll1rgY0GR/7toKQ+YVGfUkTephYhOAfomjtMjQ==
      -----END RSA PRIVATE KEY-----

deployer_ssh_public_key : Required : Sets the deployer's public key

    deployer_ssh_public_key: |+
      ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC9u2x4/VJkyxaKpVylVPILcX0RwiOVsPXxsXXxyWVezsqk33TYO0v4EuRmEm8Z690iaM7XjZynhk61kV/u4tO5tUUFFiMBMM7lRBBo2XxBok8rX81sPIljeqrVaAJvRnbrQ/oqrZe4DIJD91Vt++kjCo/EHA140urPAvIPs4eQSLt7hRO/wYB2quE439yVOxPpkdU98jPYfYRMhgS4yDG3BMp+wBqqlvWO8FSfWJQxeyV/UHxoQ7m1djsYUDqQN3Xjl1S95ZH9Eb3rWonAvQECvx3aDjfUVsyiMFFB0wb7BWOuW8kAoAFKvBmZ+YutktFO+Q1plBt2ZC/9738C1wlF innohub-insecure@innohub-ansible.vagrant

deployer_ssh_keyscan_domains : Required : Adds domains to known hosts

    deployer_ssh_keyscan_domains:
      - github.com

License
-------

MIT
