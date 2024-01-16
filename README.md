# React + TypeScript + Vite

Tseu modelo fornece uma configuração mínima para fazer o React funcionar no Vite com HMR e algumas regras ESLint.

Atualmente, dois plugins oficiais estão disponíveis:

    @vitejs/plugin-react usa Babel para atualização rápida
    @vitejs/plugin-react-swc usa SWC para atualização rápida

Expandindo a configuração do ESLint

Se você estiver desenvolvendo um aplicativo de produção, recomendamos atualizar a configuração para ativar regras de lint com reconhecimento de tipo:

    Configure a propriedade parserOptions de nível superior assim:

padrão de exportação {
  //outras regras...
  opções de analisador: {
    ecmaVersion: 'mais recente',
    sourceType: 'módulo',
    projeto: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
  },
}

    Substitua plugin:@typescript-eslint/recommended por plugin:@typescript-eslint/recommended-type-checked ou plugin:@typescript-eslint/strict-type-checked
    Opcionalmente, adicione plugin:@typescript-eslint/stylistic-type-checked
    Instale eslint-plugin-react e adicione plugin:react/recommended & plugin:react/jsx-runtime à lista estendida
