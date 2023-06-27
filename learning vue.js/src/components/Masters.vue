<template>
  <div>
    <h1>Select the Masters you want to talk to</h1>
    <div class="masters-container">
      <div
        class="master"
        v-for="master in masters"
        :key="master.name"
        @click="selectMaster(master)"
      >
        <img
          :src="master.image"
          :alt="master.name"
          :class="{ selected: master.selected }"
        />
        <p>{{ master.name }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Masters",
  data() {
    return {
      masters: [
        {
          name: "Krishna",
          image:
            "https://w0.peakpx.com/wallpaper/732/841/HD-wallpaper-krishna-god-lord-krishna-mahabharat-narayan-narayana-shri-rama-vasudeva-thumbnail.jpg",
          selected: false,
        },
        {
          name: "Jesus",
          image:
            "https://img.freepik.com/free-photo/free-photo-good-friday-background-with-jesus-christ-cross_1340-28455.jpg?w=2000",
        },
        {
          name: "Buddha",
          image:
            "https://i0.wp.com/literariness.org/wp-content/uploads/2019/04/ccc01a3100025a5531f7b2b7b5fdc462.jpg?fit=564%2C846&ssl=1",
        },
        {
          name: "Guru Nanak",
          image:
            "https://www.bhaktiphotos.com/wp-content/uploads/2021/08/Guru-Nanak-Dev-Sikh-Guru-Ji-Pics-HD-Wallpaper-Images.jpg",
        },
        {
          name: "Sadhguru",
          image:
            "https://wallpapers.com/images/hd/smiling-sadhguru-against-a-yellow-background-rqqshwt1ojaphvmc.jpg",
        },
        {
          name: "Sri Sri Ravishankar",
          image:
            "https://m.economictimes.com/thumb/msid-68770713,width-1200,height-900,resizemode-4,imgsize-144712/sri-sri-ravishankar.jpg",
        },
        {
          name: "Eckhart Tolle",
          image:
            "https://yt3.googleusercontent.com/ytc/AGIKgqNGKLiN166Wp-kO_Fsc3dPjyI1Uurr-6CB7d1tJjg=s900-c-k-c0x00ffffff-no-rj",
        },
        {
          name: "Osho",
          image:
            "https://oshoworld.com/wp-content/uploads/2020/08/oshoRajneeshpuram3.jpg",
        },
        {
          name: "Swami Vivekananda",
          image:
            "https://www.culturalindia.net/iliimages/Swami-Vivekananda-ili-96-img-1.jpg",
        },
        {
          name: "Jiddu Krishnamurthi",
          image:
            "https://yt3.googleusercontent.com/0WWNUMCZXVG0F6uANbGBac_R61i8QbPvEHij87N95-TMl4--3pb6mR2OTsHWKDpauVFk4BiKsew=s900-c-k-c0x00ffffff-no-rj",
        },
        {
          name: "Lao Tzu",
          image: "https://thecitesite.com/images/authors/lao-tzu.jpeg",
        },
        {
          name: "Dalai Lama",
          image:
            "https://yt3.googleusercontent.com/ytc/AGIKgqOVJdKe3nmD5NLLYwfq5rEzMSxFLgKFI8ABCXhbmg=s900-c-k-c0x00ffffff-no-rj",
        },
        {
          name: "Zen master Suzuki",
          image:
            "https://cdn-japantimes.com/wp-content/uploads/2022/07/np_file_168643.jpeg",
        },
        {
          name: "Sufi master Rumi",
          image:
            "https://images-na.ssl-images-amazon.com/images/I/91Z26GWkflL.jpg",
        },
        {
          name: "Socrates",
          image:
            "https://images.squarespace-cdn.com/content/v1/5c70349e348cd96170d34172/1601657651261-OV1IXR9OFYKW1RRL089H/socrates_colorized.jpeg",
        },
        {
          name: "Aristotle",
          image: "https://static.javatpoint.com/biography/images/aristotle.jpg",
        },
        {
          name: "Plato",
          image:
            "https://c8.alamy.com/comp/W5TGMY/plato-428-bc-348347-bc-greek-philosopher-student-of-socrates-founder-of-the-academy-watercolor-W5TGMY.jpg",
        },
        {
          name: "Sigmund Freud",
          image:
            "https://hips.hearstapps.com/hmg-prod/images/gettyimages-613470752jpg-13-31-39-121.jpg",
        },
        {
          name: "Carl jung",
          image:
            "https://hips.hearstapps.com/hmg-prod/images/carl-jung-9359134-1-402.jpg",
        },
      ],
    };
  },
  methods: {
    selectMaster(selectedMaster) {
      this.masters.forEach((master) => {
        if (master === selectedMaster) {
          master.selected = !master.selected;
        } else {
          master.selected = false;
        }
      });
    },
  },
};
</script>

<style scoped>
.masters-container {
  display: flex;
  max-height: 200px;
  overflow-x: scroll;
  gap: 30px;
}

.master {
  width: 200px;
  justify-content: center;
  align-items: center;
  text-align: center;
  cursor: pointer;
}

.master img {
  height: 70px;
  width: 70px;
  margin: auto;
  border-radius: 50%;
  border: 2px solid transparent;
  transition: border-color 0.3s;
}

.master img.selected {
  border-color: #f79311;
  box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px,
    rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;
}

h1 {
  padding: 1rem;
  text-align: center;
}
</style>
