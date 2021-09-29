<script lang="ts">
    import Question from './Question.svelte';

    const questions = [
        {
            q: 'What is a hackathon?',
            a: 'Hackathons are where your crazy idea becomes reality. Students work in teams of up to four for 36 ' +
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
            q: 'How big should teams be?',
            a: 'We highly encourage you to build with a team. Teamwork is deeply rooted in the hacking ethos, and ' +
                'you’ll have a better time building with your brightest peers. Teams shall consist of no more ' +
                'than four people. But don’t worry if you don’t have a team before the event — we will ' +
                'have a team-formation session Friday night.'
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
            a: 'Due to the pandemic, GunnHacks 7.0 will be held online this year. Join the <a href="https://discord.gg/ZzHuQMXRW6">Discord server</a>.'
        },
        {
            q: 'When does registration close?',
            a: 'Registration closes on February 12th, at 5pm PST, when the hackathon begins.'
        },
        {
            q: 'I’m interested in mentoring! How can I get involved?',
            a: 'Yay! Shoot us an email at <a href="mailto:ghshacks@gmail.com">ghshacks@gmail.com</a>.'
        },
        {
            q: 'What if I have another question?',
            a: 'We love questions! Please feel free to reach out to us at <a href="mailto:ghshacks@gmail.com">ghshacks@gmail.com</a>.'
        },
    ];
</script>

<section id="faq">
    <div class="content">
        <h2>FAQ</h2>

        <div class="question-grid">
            {#each questions as {q, a}}
                <Question q={q} a={a} />
            {/each}
        </div>
    </div>
</section>

<style lang="scss">
  #faq {
    font-family: 'Abel';
    background-color: #dd5d5c;
  }

  .content {
    padding: 20px;
    margin: 0 auto;
    max-width: 1024px;

    h2 {
      text-align: center;
      font-size: 3rem;
      border-bottom: 2px solid white;
      margin-top: 0;
      margin-bottom: 1rem;
    }

    .question-grid {
      display: grid;
      grid-template-columns: 50% 50%;
      grid-auto-flow: row;
    }
  }
</style>
