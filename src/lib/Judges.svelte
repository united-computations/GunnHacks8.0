<script lang="ts">
    import Section from './Section.svelte';
    import Judge from './Judge.svelte';
</script>

<Section title="Mentors and Judges" id="judges">
    <div class="judges-content">
        <Judge name="Jeff Li" title="Judge" desc="Principal Software Engineer at Microsoft" src="judges/judge_jeff_li.jpg" />
        <Judge name="Nan Zhong" title="Judge" desc="Software Engineering Manager at Google" src="judges/judge_nan_zhong.jpg" />
        <Judge name="Yun Luo" title="Judge" desc="Senior Software Engineer at Netflix" src="judges/judge_yun_luo.jpg" />
        <Judge name="Bai Wang" title="Mentor" desc="Staff Medical Imaging Engineer at Intuitive Surgical" src="judges/mentor_bai_wang.jpg" />
        <Judge name="Sean Yen" title="Mentor / Judge" desc="Gunn graduate. Likes sheep." src="judges/judge_mentor_sean.jpg" />
        <Judge name="Timothy Herchen" title="Mentor / Judge" desc="Gunn graduate. Likes cows." src="judges/judge_mentor_tim.jpg" />
        <Judge name="Yu-Ting Chang" title="Mentor" desc="Gunn student. Likes Python." />
        <Judge name="Ethan Liang" title="Mentor" desc="Gunn student" />
        <Judge name="Pranavi Prashant" title="Mentor" desc="Pioneers at technical help and cracking lame physics jokes" src="judges/mentor_pranavi.jpg"/>
        <Judge name="Atulya Weise" title="Mentor" desc="I focus on product design + development, and I enjoy sharing my skills. @atultw on GitHub." src="judges/mentor_atulya.jpg"/>
        <Judge name="Arnav Pandey" title="Mentor" desc="High school sophomore fluent in many coding languages, and experience in over 15 hackathons" src="judges/mentor_arnav.jpg"/>
    </div>
</Section>

<style lang="scss">
  .judges-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem 2.5rem;
  }
</style>
