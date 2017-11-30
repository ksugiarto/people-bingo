## People Bingo Generator

[IMG]

This is a small NodeJS application to generate People Bingo. Some called Human Bingo, so what is People Bingo?

> Human Bingo (also known as the Autograph Game or Did You Know? Bingo) is an icebreaker that helps people learn interesting facts about each other. People walk around the room and mingle until they find people that match the facts listed on a bingo-style sheet.

> This game is a get-to-know-you style icebreaker. The recommended group size is: large or extra large. The game works best with a group of about 25 people. It can be played indoors or outdoors. Materials required are: printed bingo sheets and pens. Ages 12 and up.

> _source: [link](https://www.icebreakers.ws/large-group/did-you-know-bingo.html)_

#### Installation Guide

Clone the code to your local either using ssh or https (pick one of the line below):

```bash
$ git clone git@github.com:ksugiarto/people-bingo.git
$ git clone https://github.com/ksugiarto/people-bingo.git
```

Do `npm install` to install prerequisites packages:

```bash
$ npm install
```

#### Configuration

All configurations will be using manual way, you can change those on `/views/index.ejs`.

1. By default, it will skip one page when on print dialog to avoid different margin on first page, you can change on `line 9`:

```html
<!-- h1 with height here is to skip 1 A4 page due to different header's margin on browser -->
<h1 style="height: 990px"></h1>
```

2. By default it has 35 items that will be put uniquely random on each bingo sheet at maximum to 25 items, you can change the list on `line 13`:

```javascript
var boards = [
  "Pernah katam Alkitab 5 kali",
  "Yang hari ini makan soto",
  //...
  "Bisa bahasa Perancis",
  "Alergi keju",
];
```

3. By default it will generate **60** sheets, you can change the count on `line 94`:

```javascript
for (var i = 1; i <= 60; i++) {
  getBoard();
}
```

#### Run The Generator

```bash
$ npm run start
```

Open `localhost:3000` on your browser, then do `Ctrl + p` to show browser's print dialog to print to pdf or printer directly.
