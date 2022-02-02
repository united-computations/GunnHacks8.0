<script>
    import Section from './Section.svelte';
    import ScheduleColumn from './ScheduleColumn.svelte';

    const feb5 = [
        ['12:30 PM', 'Opening Ceremony'],
        ['1:30 PM', 'Team formation activity begins'],
        ['2:00 PM', 'Hacking begins'],
        ['2:00 PM', 'Intro to Python Workshop'],
        ['4:00 PM', 'React Workshop'],
        ['6:00 PM', '!Light Activity'],
        ['9:00 PM', 'Movie Night'],
    ];
    const feb6 = [
        ['9:00 AM', 'Networking Workshop'],
        ['2:00 PM', 'Hacking ends'],
        ['2:00 PM', 'Judging starts'],
        ['4:30 PM', 'Judging ends'],
        ['5:00 PM', 'Closing ceremony'],
    ];
</script>

<Section red title="Schedule" id="schedule">
    <div class="schedule-blocks">
        <ScheduleColumn date="February 5th" schedule={feb5} />
        <ScheduleColumn date="February 6th" schedule={feb6} />
    </div>
    <p>All times are in PST.</p>
</Section>

<style lang="scss">
  .schedule-blocks {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }

  /*
  p {
    font-style: italic;
    color: rgba(255, 255, 255, 0.7);
  }
  */
</style>
