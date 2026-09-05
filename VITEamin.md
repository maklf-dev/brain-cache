# vite

```bash
node -v
```

```bash
npm -v
```

```bash
npm create vite@latest .
```

- answer:
    - Package name
    - Select a framework
    - Select a variant

## ThreeJS
- to install threeJs:

```bash
npm install three
```

- to check it:
    - html:
        ```html
        <script type="module" src="/src/main.js"></script>
        ```
    - css:
        ```css
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            overflow: hidden;
        }
        ```
    - js:
        ```js

            import * as THREE from "three";
            import "./style.css";

            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(
            75,
            window.innerWidth / window.innerHeight,
            0.1,
            1000
            );

            camera.position.z = 5;

            const geometry = new THREE.BoxGeometry();
            const material = new THREE.MeshBasicMaterial({color: 0x00ff00});
            const cube = new THREE.Mesh(geometry, material);

            scene.add(cube);

            const renderer = new THREE.WebGLRenderer();

            renderer.setSize(window.innerWidth, window.innerHeight);
            document.body.appendChild(renderer.domElement);
            renderer.render(scene, camera);
        ```