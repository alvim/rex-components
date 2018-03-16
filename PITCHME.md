# Rex Components
###### https://bitbucket.org/original-io/rex-components

---

Todos os componentes Rex são armazenados nesse repositório. A versão será controlada por meio de [versionamento semântico](https://semver.org/lang/pt-BR/).

**Todo componente deve ser documentado, sem exceção.** Um componente sem documentação, não será considerado.

**Todo componente deverá conter testes unitários.** Um componente sem TDD também não será considerado.

---

```javascript
import './index.scss'

const Banner = function(node, props = {}) {
    const options = {
         transition: 'fade', // default options
         ...props // sobreescrever default options com props
    }

    this.boxes = node.querySelectorAll('.box-banner')
}

export default Banner
```
@[1] - "Importar o scss, como sempre fazemos."
@[3-10] - "Código modular."

---

![Estrutura](http://github.com/alvimm/rex-components/blob/master/assets/print1.png?raw=true)

---

```json
{
"scripts": {
    "build": "node scripts/build.js",
    "start": "cross-env NODE_ENV=development webpack-dev-server --open --config ./webpack.config.js"
    }
}
```
@[3] - "Para gerar o build que será usado no GrapesJS."
@[4] - "Para iniciar ambiente de desenvolvimento."
