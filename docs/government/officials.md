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
    avatar: 'https://cdn.discordapp.com/avatars/168800441126092800/9a7499056a75efea8e3abc433faf291b?size=1024',
    name: "Aki",
    title: 'Alcuahtl, Councillor',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/270360642496626690/f1fbb74aae06664f9f26e015bfbbbe68?size=1024',
    name: 'x1025',
    title: 'Chieftain, Councillor',
    links: []
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/199409362781863936/97f2fdfd3755238e8d2ca1282a0d4112?size=1024',
    name: "Yergo",
    title: 'Councillor',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/168818172781264897/a3cdc309389db167bd69c05778c790dd?size=1024',
    name: "MechanicalRift",
    title: 'Councillor',
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
