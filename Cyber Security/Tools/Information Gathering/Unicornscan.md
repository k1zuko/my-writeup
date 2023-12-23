```bash
unicornscan --help
unicornscan -v -I {TARGET IP}
unicornscan -v -I -mT {TARGET IP}
unicornscan -v -I -mU {TARGET IP}
unicornscan -r500 -mT -v -I {TARGET IP}
unicornscan -r500 -mT -v -I {TARGET IP}/24:22
unicornscan -v -I -mTsA {TARGET IP}
unicornscan -v -I -mTsFPU {TARGET IP}

ls -lah /usr/lib/unicornscan/modules
unicornscan -eosdetect -mT {TARGET IP}

```