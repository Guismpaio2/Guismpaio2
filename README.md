<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=DD0031&height=120&section=header&text=Guilherme%20Sampaio&fontSize=42&fontColor=fff&fontAlignY=38&desc=Full-Stack%20%7C%20Angular%20%7C%20Game%20Dev&descAlignY=60&descSize=18&animation=fadeIn" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=DD0031&center=true&vCenter=true&width=600&lines=Arquitetando+interfaces+com+Angular+%F0%9F%94%A5;Dados+em+tempo+real+com+Firebase+%E2%9A%A1;Construindo+APIs+em+Go+e+Node.js+%F0%9F%90%B9;Game+dev+nas+horas+vagas+%F0%9F%8E%AE" alt="Typing SVG" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/guismpaio/)
[![Portfolio](https://img.shields.io/badge/Portfolio-%23000000.svg?style=for-the-badge&logo=firefox&logoColor=DD0031)](https://guismpaio2.github.io)
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/guismpaio/)
[![Gmail](https://img.shields.io/badge/Gmail-%23EA4335.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:guicsmpaio@gmail.com)

</div>

<br/>

---

## `$ whoami`

```ts
const guilherme = {
  name:     "Guilherme Sampaio",
  role:     "Full-Stack Developer & Game Dev",
  location: "Cruzeiro — SP, Brasil 🇧🇷",
  education: "Técnico em Informática · SENAI-SP",
  focus:    ["Angular", "Firebase", "TypeScript", "Clean Architecture"],
  available: true, // disponível para freelance
};
```

Desenvolvedor apaixonado por **construir sistemas que funcionam de verdade** — da camada de autenticação ao deploy em produção. Aplico **Dependency Injection**, **Service Layer Pattern** e **RBAC** no dia a dia com Angular, e exploro Go e Java quando o back-end pede mais poder. Nas horas vagas, troco o VS Code pela Unity e protipo jogos em game jams.

> _"Todo código é um sistema em construção. Todo jogo é um mundo em design."_

<br/>

---

## ⚙️ Domínios Técnicos

<details open>
<summary><b>🔺 UI Layer — interfaces que respiram</b></summary>
<br/>

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=angular,ts,html,css,scss,bootstrap,tailwind&theme=dark" />
  </a>
</p>

| Tecnologia | Uso |
|---|---|
| **Angular 14–18** | Componentização modular, Reactive Forms, Router com Guards |
| **TypeScript** | Tipagem forte, interfaces, generics, enums de domínio |
| **SCSS / Bootstrap 5** | Design system responsivo, variáveis, mixins |
| **TailwindCSS** | Utility-first em projetos de protótipo rápido |

</details>

<br/>

<details open>
<summary><b>⚡ Reatividade — dados fluindo sem parar</b></summary>
<br/>

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=rxjs&theme=dark" />
  </a>
</p>

- `BehaviorSubject` para gerenciamento de estado de autenticação reativo
- `combineLatest` + `switchMap` para joins em tempo real entre coleções Firestore
- `Observable` pipelines com `map`, `take`, `filter` no lugar de callbacks
- `AngularFireAuth.authState` como stream de autenticação persistente

</details>

<br/>

<details open>
<summary><b>☁️ Persistência & Back-end — onde os dados vivem</b></summary>
<br/>

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=firebase,mongodb,nodejs,go,java&theme=dark" />
  </a>
</p>

| Stack | Projeto / Contexto |
|---|---|
| **Firebase Auth + Firestore** | ConstructoV18 — RBAC + dados em tempo real |
| **MongoDB + Node.js** | API-Mongo — REST CRUD com persistência NoSQL |
| **Go (Golang)** | CRUD-GO — exploração de performance e concorrência |
| **Java** | ProjetoSoftware-Java — modelagem OO e design de classes |

</details>

<br/>

<details open>
<summary><b>🎮 Game Dev & Ferramentas</b></summary>
<br/>

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=unity,cs,git,vscode&theme=dark" />
  </a>
</p>

- **Unity + C#** · desenvolvimento de mecânicas de jogo, prototipagem em game jams
- **Git** · fluxo com branches, commits semânticos, versionamento de projetos

</details>

<br/>

---

## 🚀 Projetos

### 🏗️ ConstructoV18 — Sistema de Estoque Empresarial
> `Angular 18` `Firebase` `TypeScript` `Bootstrap 5` `RxJS` `ngx-toastr`

[![Repositório](https://img.shields.io/badge/Ver%20Repositório-DD0031?style=flat-square&logo=github&logoColor=white)](https://github.com/Guismpaio2/ConstructoV18)

<table>
<tr>
<td width="50%">

**O que é**

Sistema completo de gerenciamento de estoque com múltiplos perfis de usuário, CRUD de produtos/estoque/baixas e deploy no Firebase Hosting.

**Funcionalidades**
- 🔐 Autenticação via Firebase Auth (login, cadastro, recuperação de senha)
- 👥 RBAC: `Administrador` · `Estoquista` · `Leitor`
- 📦 CRUD de produtos, itens de estoque e registros de baixas
- 📊 Dashboard com visão gerencial do estoque
- ☁️ Deploy no Firebase Hosting

</td>
<td width="50%">

**Decisões Arquiteturais**

```
src/app/
├── auth/
│   ├── auth.service.ts   ← BehaviorSubject + switchMap
│   └── auth.guard.ts     ← CanActivate com RBAC por rota
├── services/             ← Service Layer Pattern
│   ├── produto.service.ts  ← DTO mapping Firestore↔App
│   └── estoque.service.ts  ← combineLatest para joins
├── models/               ← Domain models tipados
│   ├── user.model.ts       ← UserRole como union type
│   └── produto.model.ts    ← ProdutoFirestore vs Produto
└── shared/               ← Componentes reutilizáveis
```

</td>
</tr>
</table>

<details>
<summary><b>🔍 Deep Dive técnico</b></summary>
<br/>

**RBAC com AuthGuard**
Cada rota declara `data: { roles: UserRole[] }`. O guard consome `user$` como Observable e verifica a role via `pipe(take(1), map(...))` — redireciona para `/home` se não autorizado, nunca bloqueia sem feedback.

```ts
// auth.guard.ts
return this.authService.user$.pipe(
  take(1),
  map((user) => {
    if (user && requiredRoles.includes(user.role)) return true;
    return this.router.createUrlTree(['/home']); // RBAC declarativo por rota
  })
);
```

**Estado Reativo com BehaviorSubject**
`AuthService` mantém `_userRole` como `BehaviorSubject<string | null>`, atualizado pelo stream `afAuth.authState` via `switchMap`. Métodos como `isAdmin()` derivam Observables desse subject — zero polling.

```ts
// auth.service.ts
private _userRole = new BehaviorSubject<string | null>(null);

isAdmin(): Observable<boolean> {
  return this._userRole.asObservable().pipe(map(role => role === 'Administrador'));
}
```

**Repository Pattern + DTO Mapping**
`ProdutoService` usa métodos privados `convertFirestoreToAppProduto` e `convertAppToFirestoreProduto` para isolar o formato do Firestore do modelo de domínio — as páginas nunca lidam com `ProdutoFirestore` diretamente.

```ts
// produto.service.ts — DTO privado, domínio público
private produtosCollection: AngularFirestoreCollection<ProdutoFirestore>;

getProduto(uid: string): Observable<Produto> {      // ← modelo de domínio
  return this.produtosCollection.doc(uid).valueChanges().pipe(
    map(data => this.convertFirestoreToAppProduto(data)) // ← mapeamento interno
  );
}
```

**Join em Tempo Real**
`EstoqueService.getEstoqueItems()` usa `combineLatest` sobre N observables de `getProduto()`, enriquecendo cada item com dados do produto — join declarativo, sem SQL.

```ts
// estoque.service.ts
const produtoObservables = items.map(item =>
  this.produtoService.getProduto(item.produtoUid).pipe(
    map(produto => ({ ...item, nomeProduto: produto?.nome }))
  )
);
return combineLatest(produtoObservables); // ← join reativo de N coleções
```

</details>

<br/>

---

### 📖 Pokédex — Angular + PokéAPI
> `Angular` `TypeScript` `SCSS` `REST API`

[![Repositório](https://img.shields.io/badge/Ver%20Repositório-DD0031?style=flat-square&logo=github&logoColor=white)](https://github.com/Guismpaio2/Pokedex)

Pokédex interativa consumindo a PokéAPI. Integração com API REST pública, interface responsiva com SCSS e componentes Angular reutilizáveis.

<br/>

---

### 🌐 API MongoDB — REST + Node.js
> `Node.js` `JavaScript` `MongoDB` `REST API`

[![Repositório](https://img.shields.io/badge/Ver%20Repositório-DD0031?style=flat-square&logo=github&logoColor=white)](https://github.com/Guismpaio2/API-Mongo)

API REST completa com rotas CRUD (GET · POST · PUT · DELETE) e persistência no MongoDB. Estudo prático de back-end Node.js orientado a documentos.

<br/>

---

### 🐹 CRUD em Go — Performance e Concorrência
> `Go` `Golang` `CRUD`

[![Repositório](https://img.shields.io/badge/Ver%20Repositório-DD0031?style=flat-square&logo=github&logoColor=white)](https://github.com/Guismpaio2/CRUD-GO_Estudo)

Exploração da linguagem Go para CRUD de alta performance. Foco em tipagem estática, goroutines e a leveza do runtime Go comparado ao Node.js.

<br/>

---

### 🎮 Ludum Dare Jam — Game Dev em 72h
> `Unity` `C#` `Game Development`

[![Repositório](https://img.shields.io/badge/Ver%20Repositório-DD0031?style=flat-square&logo=github&logoColor=white)](https://github.com/Guismpaio2/LudumDareJam)

Jogo prototipado do zero em 72 horas para a Ludum Dare. Mecânicas implementadas com C# + Unity, onde a restrição de tempo é o verdadeiro desafio de design.

<br/>

---

## 📊 Stats

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=Guismpaio2&show_icons=true&theme=radical&include_all_commits=true&count_private=true&hide_border=true&bg_color=0d1117&title_color=DD0031&icon_color=DD0031" />
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Guismpaio2&layout=compact&langs_count=8&theme=radical&hide_border=true&bg_color=0d1117&title_color=DD0031" />

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=Guismpaio2&theme=radical&hide_border=true&background=0d1117&ring=DD0031&fire=DD0031&currStreakLabel=DD0031&locale=pt_BR)](https://git.io/streak-stats)

</div>

<br/>

---

## 🎓 Formação

<table>
<tr>
<td>🏫 <b>SENAI — SP</b></td>
<td>Técnico em Informática + Cursos Complementares</td>
</tr>
</table>

---

## 📫 Contato

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/guismpaio/)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:guicsmpaio@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Guismpaio2)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/guismpaio/)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF4500?style=for-the-badge&logo=firefox&logoColor=white)](https://guismpaio2.github.io)

</div>

<br/>

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=Guismpaio2&label=Visitas+ao+Perfil&color=DD0031&style=flat-square" />
</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=DD0031&height=80&section=footer" />
