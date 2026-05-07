---
layout: page
---

<script setup>
import {
  VPTeamPage,
  VPTeamPageTitle,
  VPTeamMembers,
} from 'vitepress/theme'

const members = [
  {
    avatar: 'https://cdn.discordapp.com/guilds/278045721742147586/users/168818172781264897/avatars/a_313bbb73d711f29ed8a78d2b63b532ce.webp?size=1024',
    name: "MechanicalRift",
    title: 'Alcuahtl, Councillor',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/565974620243755010/dba32173e5fbcfe7391b6e9163c48399.webp?size=1024',
    name: 'LeafChalice',
    title: 'Councillor'
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/896387305374375987/33d9b66ad68747efe0a2e9a39a79c011.webp?size=1024',
    name: "1Stev0",
    title: 'Councillor',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/695983093022064762/34e19766c655237ee048dcb1457e2bee.webp?size=1024',
    name: "Pikaboos",
    title: 'Councillor',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/1268295797540388926/c800a2c92194b5f84db52af00754650e.webp?size=1024',
    name: "Ant",
    title: 'Councillor'
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/314198862560493569/75c0774c2784fc9ad5fb3d4d0a7eb80a?size=1024',
    name: "Feathercrown",
    title: 'High Justice',
  },
]

const day = new Date();
if (day.getMonth()+1 === 4 && day.getDate() === 1) {
    members.forEach((member) => {
    member.title = member.title.replace("Alcuahtl", "Axolotl");
  })
}
</script>

<VPTeamPage>
  <VPTeamPageTitle>
    <template #title>
      Government Officials
    </template>
    <template #lead>
        Yoahtl is comprised of people from around the world,
        and those listed below are among those who hold official jobs within it.
    </template>
  </VPTeamPageTitle>
  <VPTeamMembers
    :members="members"
  />
</VPTeamPage>
