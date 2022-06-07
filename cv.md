# __[rsschool-cv](https://webkwondo.github.io/rsschool-cv/)__

# __Elena Markova__

## __Contacts__
- __Discord:__ webkwondo#7413
- __t.me:__ [@webkwondo](https://t.me/webkwondo)
- __GitHub:__ [webkwondo](https://github.com/webkwondo)

## __About Me__
I'm passionate and experienced web-developer, formerly a web-designer.
I build custom websites and provide design solutions for small- and middle-scaled web-projects.
I like beautiful, user centered design, accessibility, clean and efficient code.

## __Skills__
- HTML5
- Pug, Twig
- CSS3 (SCSS, LESS)
- SVG
- JavaScript
- JQuery (legacy)
- Node.js
- Git, SVN
- Gulp
- Webpack
- PHP, MySQL
- WordPress
- Adobe Photoshop (level – Experienced), Figma
- Pixel Perfect
- Web Performance

## __Code Example__
```
export const performCalculations = async () => {
  const fileName = 'worker.js';
  const filePath = join(__dirname, fileName);
  const cpuCount = cpus().length;
  let number = 10;

  const createWorker = (data) => {
    return new Promise((resolve, reject) => {
      const worker = new Worker(filePath, {
        workerData: data
      });

      worker.on('message', (msg) => {
        if (typeof msg === 'number') {
          resolve({status: 'resolved', data: msg});
        } else {
          resolve({status: 'error', data: null});
        }
      });

      worker.on('error', (msg) => {
        reject({status: 'error', data: null});
      });

      worker.on('exit', (code) => {
        if (code !== 0) {
          reject({status: 'error', data: null});
        }
      });
    });
  };

  const promises = [];

  for (let i = 0; i < cpuCount; i++, number++) {
    promises.push(createWorker(number));
  }

  const results = (await Promise.allSettled(promises)).map((result) => {
    if (result.status === 'fulfilled') {
      return result.value;
    }

    if (result.status === 'rejected') {
      return result.reason;
    }
  });

  return results;
};

const res = await performCalculations();
```

## __Experience__
- Working with outsourcing companies
- Freelancing
- Project-management

## __Education__
- __University:__ Financial University, Economics major
- __Courses:__
  - [HTML Academy full frontend-developer course](https://www.htmlacademy.ru)
  - [CS50 lectures](https://www.youtube.com/channel/UCcabW7890RKJzL968QWEykA)

## __English__
__C1__ (Advanced)
