<template>
    <div>
    <ProfileHeader/>
    <ProfileAbout/>
    <ProfileTechnicalskills/>
    <ProfileWorkExperience/>
    <ProfileContact/>
    <ProfileFooter/>
    

    </div>
</template>
<script >
import ProfileHeader from '@/components/ProfileHeader.vue'
import ProfileAbout from '@/components/ProfileAbout.vue';
import ProfileTechnicalskills from '@/components/ProfileTechnicalskills.vue';
import ProfileWorkExperience from '@/components/ProfileWorkExperience.vue';
import ProfileContact from '@/components/ProfileContact.vue';
import ProfileFooter from '@/components/ProfileFooter.vue';



export default{
    component: {
        ProfileHeader,
        ProfileAbout,
    ProfileFooter,
    ProfileContact,
    ProfileTechnicalskills,
    ProfileWorkExperience



    },
    components: { ProfileHeader, ProfileFooter, ProfileContact, ProfileTechnicalskills, ProfileAbout, ProfileWorkExperience }
};
</script>