<template>
    <div class="contact-set">
        <a :href="contact.link" class="contact-item" v-for="contact in contacts" :key="contact.name" target="_blank">
            <img :src="require('../assets/img/icons/' + contact.img)" width="20" height="20" :alt="contact.name" loading="lazy">
            {{contact.text}}
        </a>
    </div>
</template>

<script>
export default {
    name: 'ContactSet',
    data() {
        return {
            contacts: [
                {
                    name: 'location',
                    text: 'Singapore',
                    img: 'location.png',
                },
                
                {
                    name: 'email',
                    text: 'HenryKey221@gmail.com',
                    img: 'email.png',
                  
                },
                {
                    name: 'phone',
                    text: '952 373 5638',
                    img: 'phone.png',
                    link: 'tel:+1 952 373 5638'
                },
                {
                    name: 'skype',
                    text: 'My skype address:     live:.cid.99f6eb13edc73001',
                    img: 'skype.png',
                },
            ]
        }
    }
}
</script>

<style>
.contact-set {
    width: 100%;
}
.contact-item {
	display: flex;
  align-items: center;
  padding: 1.6rem;
  border: 1px solid hsla(0, 0%, 100%, 0.2);
  background-color: var(--main-bg-color);
  backdrop-filter: blur(5px);
  border-radius: var(--box-border-radius);
  border: var(--box-border);
  box-shadow: var(--box-shadow);
  margin-bottom: .3rem;
  transition: all .2s ease
}
.contact-item:hover {
	background-color: var(--contact-item-hover-bg);
  border: var(--box-border);
}
.contact-item img {
	margin-right: 1.5rem;
  height: auto;
  filter: drop-shadow(var(--regular-text-shadow))
}
@media (max-width: 600px) {
  .contact-item {
    padding: 1rem;
    font-size: 0.9rem;
  }
}
@media (max-width: 350px) {
  .contact-item {
    padding: 1.5rem .8rem;
    font-size: 0.9rem;
  }
  .contact-item img {
    margin-right: .5rem;
  }
}
</style>