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
    avatar: 'https://cdn.discordapp.com/avatars/834536107878121542/d3e84cb849dc40c34504d9038ca74d40?size=1024',
    name: 'Arconis',
    title: 'Alcuahtl, Councillor',
    links: []
  },
  {
    avatar: "https://cdn.discordapp.com/avatars/528230329454952478/a_fe45d0fd7bd63f2df1dc0ed01fdaa3d9?size=1024",
    name: "Awesome_Daniel",
    title: 'Councillor',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/292506314075275274/7dacdaee62825da51927ea05740b091b?size=1024',
    name: "Nukinmouse01",
    title: 'Councillor',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/270360642496626690/9b215e96c56bf570d12f0f004e70978a?size=1024',
    name: "x1025",
    title: 'Councillor',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/208052614347227138/4c34d8d9ace0a234d682983f28f0a768?size=1024',
    name: "ArkenX",
    title: 'General',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/168818172781264897/a3cdc309389db167bd69c05778c790dd?size=1024',
    name: "MechanicalRift",
    title: 'Cheiftain',
  },
  {
    avatar: 'https://cdn.discordapp.com/avatars/280815367662731266/bbfd384a75256e5cb22c4f4c294a0960?size=1024',
    name: "Husky",
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
        and those listed below are among those who hold offical jobs within it.
    </template>
  </VPTeamPageTitle>
  <VPTeamMembers
    :members="members"
  />
</VPTeamPage>
