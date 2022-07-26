# Node.js-Work2
//Patika.dev
Ödev-2-
![image](https://user-images.githubusercontent.com/71225955/180971991-fb81dbe9-354d-4901-a055-7fa50f8a967a.png)
// Array oluşturuldu
const Posts = [
    { Ders:"Matematik", Not: "90" },
    { Ders: "Fizik", Not: "75" },
    { Ders: "Kimya", Not: "100" },
    { Ders: "biyoloji", Not: "67" },
    { Ders: "Laboratuvar", Not: "88" },

  ];
  // yeni post oluşturuldu ve sıralama işlemleri yapıldı.
  const listPosts = () => {
    Posts.map((post) => {
      console.log("Ders: ", post.Ders, "Not: ", post.Not);
    });
  };
  
  const addpost = (newpost) => {
    const promise1 = new Promise((resolve, reject) => {
      Posts.push(newpost);
      resolve(Posts);
      reject('BIR HATA Meydana GEldi');
    });
  
    return promise1;
  };
  
  async function showpost() {
    try {
      await addpost({ Ders:"Kuantum Mekaniği", Not: "90" });
      listPosts();
    } catch (error) {
      console.log(error);
    }
  }

  showpost();
