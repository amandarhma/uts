<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Petunjuk Bagi Manusia</template>

    Al Quran adalah kitab suci yang diwahyukan Allah SWT kepada Nabi Muhammad
    Saw sebagai rahmat dan petunjuk bagi manusia yang beriman dan bertakwa dalam
    hidup dan kehidupannya.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Sumber Pokok Ajaran Islam</template>

    Sebab dari Al Quranlah diambil segala pokok syariat dan dalil-dalil syar'i
    yang mencakup seluruh aspek hukum bagi manusia dalam menjalani hidup di
    dunia atau di akhirat.

    <br />

  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Pengajaran bagi Manusia</template>

    Al Quran adalah pengajaran bagi manusia. Karena itu manusia mengetahui jalan
    yang hak dan batil, antara yang benar dan yang sesat dan lainnya.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Abstrak</template>

    Al Quran terdiri atas 30 juz, 114 surat, 6.236 ayat.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Manfaat Dalam Kehidupan</template>

    dapat menenangkan pikiran dan batin serta cara agar hati tenang dan dapat
    pula menjadikan rasa cinta terhadap Allah SWT, semua Nabi dan Rasul serta
    para Malaikat menjadi lebih kuat.
  </WelcomeItem>
</template>
