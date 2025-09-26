<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>おすすめAVサイト集</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f4f4f4; }
    header { background: #222; color: #fff; padding: 1rem; text-align: center; }
    .container { max-width: 1000px; margin: 2rem auto; padding: 1rem; }
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1rem; }
    .card { background: #fff; border-radius: 10px; overflow: hidden; box-shadow: 0 2px 5px rgba(0,0,0,0.1); transition: transform 0.2s; }
    .card:hover { transform: scale(1.03); }
    .card img { width: 100%; height: 160px; object-fit: cover; }
    .card-content { padding: 1rem; }
    .card-content h3 { margin: 0; font-size: 1.2rem; }
    .card-content p { font-size: 0.9rem; color: #555; }
    .overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.9); display: flex; justify-content: center; align-items: center; z-index: 9999; }
    .modal { background: #fff; padding: 2rem; border-radius: 10px; text-align: center; }
    .modal button { margin: 0.5rem; padding: 0.5rem 1rem; font-size: 1rem; border: none; border-radius: 5px; cursor: pointer; }
    .yes { background: #28a745; color: #fff; }
    .no { background: #dc3545; color: #fff; }
  </style>
</head>


  <header>
    <h1>おすすめAVリンク集</h1>
  </header>
  <div class="container">
    <div class="grid" id="card-container"></div>
  </div>

  <script>
    const data = [
      {
        title: "シンプルにかわいい",
        thumbnail: "https://via.placeholder.com/300x180.png?text=AV01",
        description: "AV01からのリンク",
        url: "https://www.av01.tv/jp/video/171095"
      },
      {
        title: "王道涼森",
        thumbnail: "https://tktube.com/ja/videos/273280/abf-159/",
        description: "tktubeのリンク1",
        url: "https://tktube.com/ja/videos/273280/abf-159/"
      },
      {
        title: "PPPE-104 ",
        thumbnail: "https://tktube.com/ja/videos/218239/pppe-104-fuck2/",
        description: "tktubeのリンク2",
        url: "https://tktube.com/ja/videos/218239/pppe-104-fuck2/"
      }
    ];

    const container = document.getElementById("card-container");
    data.forEach(item => {
      const card = document.createElement("div");
      card.className = "card";
      card.innerHTML = `
        <a href="${item.url}" target="_blank">
          <img src="${item.thumbnail}" alt="${item.title}">
          <div class="card-content">
            <h3>${item.title}</h3>
            <p>${item.description}</p>
          </div>
        </a>
      `;
      container.appendChild(card);
    });

    function enterSite() {
      document.getElementById("age-overlay").style.display = "none";
    }
    function denySite() {
      alert("18歳未満の方は利用できません。");
    }
  </script>
</body>
</html>
