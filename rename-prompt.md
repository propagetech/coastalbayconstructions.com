You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "9th-Avenue.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "9th Avenue Residence"
    }
  },
  {
    "path": "Baba-Estates.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "Baba Estates"
    }
  },
  {
    "path": "Drive-in-Restaurant.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "Drive In Restaurant"
    }
  },
  {
    "path": "Kohinoor-Plaza.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "Kohinoor Plaza"
    }
  },
  {
    "path": "Noorani-Plaza.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "Noorani Plaza"
    }
  },
  {
    "path": "Proposed-Ware-House.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "Proposed Ware House"
    }
  },
  {
    "path": "Rab-Estates-Gangoor.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "RAB ESTATES GANGOOR"
    }
  },
  {
    "path": "Sultan-Plaza.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "SULTAN PLAZA"
    }
  },
  {
    "path": "Upcoming-Warehouses-Hub.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "Upcoming Warehouses Hub"
    }
  },
  {
    "path": "VILLA.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "Villa in Mangalagiri"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "ABOUT US | WE PROVIDE THE ENTIRE LIFE CYCLE OF PROPERTIES",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "CONTACT US | GET TAILORMADE DESIGN CONCEPTS",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/4957171073492227171d872757d04770.css",
    "context": {
      "path": "css/4957171073492227171d872757d04770.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "how-it-works.html",
    "context": {
      "title": "HOW IT WORKS | RELAX AS WE MANAGE COMPLETE INSTALLATION",
      "first_heading": "HOW IT WORKS"
    }
  },
  {
    "path": "imgs/04cd26a7e71848a5ebf8e88a2669b63b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/0765e293f8b2c1981f97dec2ce9d71e6.webp",
    "context": {
      "refs": [
        {
          "alt": "4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/087552cb9be39930653974f8a650f1c8.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/09f5afb4f2bbc5a8b0f4546814120e16.webp",
    "context": {
      "refs": [
        {
          "alt": "7",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0d95798f178e0b50251cdb1025d47105.webp",
    "context": {
      "refs": [
        {
          "alt": "14",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/104501b515dfa760f56beaf9395db7bb.webp",
    "context": {
      "refs": [
        {
          "alt": "9th AVENUE",
          "title": ""
        },
        {
          "alt": "10",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/11cbed0f1e0c32e234fdb62e0c188778.webp",
    "context": {
      "refs": [
        {
          "alt": "2",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/151c156824ed7c641041b53f0650151b.webp",
    "context": {
      "refs": [
        {
          "alt": "006",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/153ff80ec80baed88bc26976d8e60abb.webp",
    "context": {
      "refs": [
        {
          "alt": "7",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/223902e6f6d7fc7a93412224bfce3695.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22df260f2fbc13a337db41e088cced17.webp",
    "context": {
      "refs": [
        {
          "alt": "6",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/24009890669571f9aaa866345a470169.webp",
    "context": {
      "refs": [
        {
          "alt": "UPCOMING WAREHOUSES HUB",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b1292712c9bb03e420e6690a94940d1.webp",
    "context": {
      "refs": [
        {
          "alt": "2",
          "title": ""
        },
        {
          "alt": "VILLA IN MANGALAGIRI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2fc7566842cd76ef9d77120a5189c836.webp",
    "context": {
      "refs": [
        {
          "alt": "010",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/371cd9c4752fd50d6a72cd0cba994035.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3ac904aab638e6ceb6ec8253497985b6.webp",
    "context": {
      "refs": [
        {
          "alt": "3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e39582987706d41db721482687f8a62.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3eea28ac3d0ad22e426804fc0c63bbef.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/40ec118479b5ab73a119da067c916f11.webp",
    "context": {
      "refs": [
        {
          "alt": "001",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/421c9fc8953b2202f405db42c2d59b6e.webp",
    "context": {
      "refs": [
        {
          "alt": "10",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42a9220dbf4768ecad36ab88fe62be17.webp",
    "context": {
      "refs": [
        {
          "alt": "009",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46cb29c34607de7e26a859e39f32da6e.webp",
    "context": {
      "refs": [
        {
          "alt": "3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4fba71d5b2255d2ba88d5b8a122a6224.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4fe9c4cf8e0d2f9bfe9ff0a6069c082f.webp",
    "context": {
      "refs": [
        {
          "alt": "2",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a5772c7132377a8cf71fee8dea49df8.webp",
    "context": {
      "refs": [
        {
          "alt": "3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ada468b01e9602dee4460121b273daf.webp",
    "context": {
      "refs": [
        {
          "alt": "2",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/651862d02699809f61f75d6b786aed52.webp",
    "context": {
      "refs": [
        {
          "alt": "013",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66e93372ce51df73affb0d210915ab92.webp",
    "context": {
      "refs": [
        {
          "alt": "KOHINOOR PLAZA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67b413da710cae82ef227ca47c854959.webp",
    "context": {
      "refs": [
        {
          "alt": "BABA ESTATES",
          "title": ""
        },
        {
          "alt": "1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6bdec06ae5ea7070a93fdb48f563741b.webp",
    "context": {
      "refs": [
        {
          "alt": "003",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6c5fce2ca978ee2f59ce06106269ebc4.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6cf7bb0795b141cdb932f793afc47524.webp",
    "context": {
      "refs": [
        {
          "alt": "4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6da93c6a015c7c48a55c38d3a4cb324f.webp",
    "context": {
      "refs": [
        {
          "alt": "10",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70e45099ac621506b1847ee5ff34b87e.webp",
    "context": {
      "refs": [
        {
          "alt": "005",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/71e9fa24bca456631fefe8c6f03f2351.webp",
    "context": {
      "refs": [
        {
          "alt": "YOUR INTERIORS, CREATED WITH PRECISION AND CARE",
          "title": ""
        },
        {
          "alt": "barcelona18685701280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7447f7f24c2019af51a26f1042e4a0f6.webp",
    "context": {
      "refs": [
        {
          "alt": "2",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76ed917483714fdc00514eaaf10c0e0e.webp",
    "context": {
      "refs": [
        {
          "alt": "5",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/778ce088b476a3490d58caa02448e0e9.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/78fdd84b382b1e103f62d8689c3e5096.webp",
    "context": {
      "refs": [
        {
          "alt": "barcelona18685701280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/79630da6a1c2b0934e4d0e1de256e1a8.webp",
    "context": {
      "refs": [
        {
          "alt": "6",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c18a3e2a1a2faddc60d0ef78b2ab15b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7d2d3a4941888c7821247dcf8da7047a.webp",
    "context": {
      "refs": [
        {
          "alt": "4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7dbdf3afb2188732be4056bf86f7bbfd.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/8238f1243c780f744e10cbd4b6292946.webp",
    "context": {
      "refs": [
        {
          "alt": "barcelona18685701280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8540428186754b92a96bee02b86fd486.webp",
    "context": {
      "refs": [
        {
          "alt": "value beyond expectation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88f66ebe8082070699847ee6394609ed.webp",
    "context": {
      "refs": [
        {
          "alt": "5",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8ad52d64b21a42b5790df2952014fe42.webp",
    "context": {
      "refs": [
        {
          "alt": "RAB ESTATES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8db24c5eab1c098194b5cce7bb40d909.webp",
    "context": {
      "refs": [
        {
          "alt": "3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/968e2acc3f92c5fa7c03ffe93ad90cc0.webp",
    "context": {
      "refs": [
        {
          "alt": "1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/98d048157833e846710898487cf450dc.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/9a69d52a200c109c810bb2f11cc3a973.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "DRIVE IN RESTAURANT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9a7ac32bc86faa2caba73cf290c59bfb.webp",
    "context": {
      "refs": [
        {
          "alt": "1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ac690af82a7ac3bad38dc31f836e6c0.webp",
    "context": {
      "refs": [
        {
          "alt": "13",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a490f104164a21f043b30ed302f2b591.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/aa4ffea947b4993a1dba7c4c6cd836c8.webp",
    "context": {
      "refs": [
        {
          "alt": "007",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aed3a26b54b3036234194dc15d735889.webp",
    "context": {
      "refs": [
        {
          "alt": "1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/afb4a2ef5ff772bd17b7cc53c55d24c8.webp",
    "context": {
      "refs": [
        {
          "alt": "barcelona18685701280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0dc1228f2c289cb6d03084943206cf0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b4f4a9a7ee7e88bb7ccc522378a56555.webp",
    "context": {
      "refs": [
        {
          "alt": "3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5721aca08135b6e061e17fae4016faa.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b97851f6b8195e3ffc693779fea8bda4.webp",
    "context": {
      "refs": [
        {
          "alt": "1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9832ce1e3dabce86326d05cacb89f43.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/ba7acb947f805c65e5cf7aa2010e0662.webp",
    "context": {
      "refs": [
        {
          "alt": "5",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bab1d8d838ba272bbb5dcdc3fa2724b3.webp",
    "context": {
      "refs": [
        {
          "alt": "NOORANI PLAZA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bb4352cc90cfdd71d4e26808350b9978.webp",
    "context": {
      "refs": [
        {
          "alt": "3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc26b60905a3cde8bd01d4872187a47a.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/bd3150eb194e55fa6a7516e58029d61b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bd8fa365ee86d187ffd04647f561a28d.webp",
    "context": {
      "refs": [
        {
          "alt": "8",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/be7b3ee99b12fa939c35a0e1c9b6c367.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c1ec2177520de19f711646ff95f865e6.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c2aa72721b5f656d6ceb916b1efe5bbb.webp",
    "context": {
      "refs": [
        {
          "alt": "2",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c33b22e4de66220ec8c7f2b6c20b48ad.webp",
    "context": {
      "refs": [
        {
          "alt": "7",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c50d719b26345f0b0e605814de0125f8.webp",
    "context": {
      "refs": [
        {
          "alt": "5",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cbe11679cf8bf2d9116441c5b7b9acf8.webp",
    "context": {
      "refs": [
        {
          "alt": "7",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dab71c52af3cd9d5f1202235713d16fc.webp",
    "context": {
      "refs": [
        {
          "alt": "7",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dc0a5c9ee6c492c2b1f95a0854942351.webp",
    "context": {
      "refs": [
        {
          "alt": "barcelona18685701280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de80fb78aa10f51727c2b868a09147ca.webp",
    "context": {
      "refs": [
        {
          "alt": "1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e61e9f88c2c3f2e64d8f9dba1ff42cb6.webp",
    "context": {
      "refs": [
        {
          "alt": "barcelona18685701280",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e79256387a2cb1943ab2315fd3332a2a.webp",
    "context": {
      "refs": [
        {
          "alt": "6",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e7a8ddfc72fa5b6936982343b551be90.webp",
    "context": {
      "refs": [
        {
          "alt": "2",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec219b483438392005684c02531226de.webp",
    "context": {
      "refs": [
        {
          "alt": "4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0c0ad8ada79850dfd20b7e492897629.webp",
    "context": {
      "refs": [
        {
          "alt": "008",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0f3c7106799a59188db407b77eda9f6.webp",
    "context": {
      "refs": [
        {
          "alt": "1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f87c7e54547d438b46cdfa4aa96829f8.webp",
    "context": {
      "refs": [
        {
          "alt": "PROPOSED WARE HOUSE",
          "title": ""
        },
        {
          "alt": "15",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f9360774e08deca966c15662ee463555.webp",
    "context": {
      "refs": [
        {
          "alt": "SULTAN PLAZA",
          "title": ""
        },
        {
          "alt": "3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f945bd31cc4c9f7ea816e0592b1bc421.webp",
    "context": {
      "refs": [
        {
          "alt": "4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbf80aca16b562eab6cf681f0ed36ab4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe66a0ce7e6e169e66af6b34c6e38648.webp",
    "context": {
      "refs": [
        {
          "alt": "011",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Home | COASTAL BAY CONSTRUCTIONS",
      "first_heading": "COASTAL BAY CONSTRUCTIONS"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/212d8155e490ffe4ae49d33bf305c1ec.js",
    "context": {
      "path": "js/212d8155e490ffe4ae49d33bf305c1ec.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "projects.html",
    "context": {
      "title": "PROJECTS | We are here to build our Nation.",
      "first_heading": "PROJECTS"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "SERVICES | ARCHITECTURAL DESIGNING, STRUCTURAL DESIGNING, INTERIOR DESIGNING, LANDSCAPE DESIGNING, CIVIL CONTRACTS",
      "first_heading": "SERVICES"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.