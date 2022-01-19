<script lang="ts">
    import Section from './Section.svelte';
    import Question from './Question.svelte';

    const questions = [
        {
            q: 'What is a hackathon?',
            a: 'Hackathons are where your crazy idea becomes reality. Students work in teams of up to four for 24 ' +
                'hours to create something amazing. Build anything — there are no restrictions on what you can create. ' +
                'Dive in and make the most incredible thing you can alongside fellow creators.'
        },
        {
            q: 'Who can attend?',
            a: 'Any high schoolers can attend GunnHacks. Unfortunately, we cannot allow college students ' +
                'or middle schoolers to attend this time around, and we cannot ship swag/prizes internationally. ' +
                'International participants are not eligible for prizes or swag.'
        },
        {
            q: 'What if I don’t know how to code?',
            a: 'All students regardless of coding ability or experience are welcome. Hackathons are a great place to ' +
                'learn, so come and build your first app, website, or anything else! We’ll also have workshops ' +
                'for you to start off or learn something new.'
        },
        {
            q: 'What can I build?',
            a: 'Web, mobile, hardware, you name it — any type of project is welcome. Projects will be judged based ' +
                'on creativity, technical difficulty, polish, and utility by a panel of industry judges.'
        },
        {
            // Update with team formation event info when that becomes available
            q: 'How big should teams be?',
            a: 'We highly encourage you to build with a team. Teamwork is deeply rooted in the hacking ethos, and ' +
                'you’ll have a better time building with your brightest peers. Teams should consist of no more ' +
                'than four people.'
        },
        {
            q: 'What if I don’t have a team?',
            a: 'No problem! Many hackers do not have a fully-formed team or hack concept before the event begins. We ' +
                'will be hosting team-forming activities before hacking begins to help you find the perfect match. If ' +
                'you’re a first-time hacker, there will be many others looking for team members with whom you can work.'
        },
        {
            q: 'How much does it cost?',
            a: 'Participation in GunnHacks is completely free. However, due to the online nature of the ' +
                'event, we recommend ownership of a computer and access to the internet.'
        },
        {
            q: 'Do I have to work the whole time?',
            a: 'No, not at all! We will have fun activities and workshops you can participate in when ' +
                'you want to take a break.'
        },
        {
            q: 'Where is GunnHacks?',
            a: 'Due to the pandemic, GunnHacks 8.0 will be held online for all participants.'
        },
        {
            q: 'When does registration close?',
            a: 'Registration will close on February 4th, 2022 at 11:59pm PST, when the hackathon begins.'
        },
        {
            q: 'I’m interested in mentoring! How can I get involved?',
            a: 'Yay! Fill out our mentor application form <a href="https://forms.gle/Rc2QsxPrDN6Hv1uLA">here</a>.'
        },
        {
            q: 'What if I have another question?',
            a: 'We love questions! Please feel free to reach out to us at <a href="mailto:ghshacks@gmail.com">ghshacks@gmail.com</a>.'
        },
    ];
</script>

<Section red title="FAQ" id="faq">
    <div class="question-grid">
        {#each questions as {q, a}}
            <Question {q} {a} />
        {/each}
    </div>
</Section>

<style lang="scss">
  .question-grid {
    display: grid;
    grid-template-columns: 50% 50%;
    grid-auto-flow: row;
    text-align: left;

    @media (max-width: 640px) {
      grid-template-columns: 100%;
    }
  }
</style>
