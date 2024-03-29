# nRF Habit Tracker

This repository is used for managing the nRF Habit Tracker project and its discussions.
The project itself is split into three other repositories.

- [Frontend repository](https://github.com/IT2901Nordic2024/frontend)
- [Backend repository](https://github.com/IT2901Nordic2024/backend)
- [Firmware repository](https://github.com/IT2901Nordic2024/firmware)

Even though the project is split into three different repositories, they combine to make the finished product which is a [user-configurable personal habit tracker.](https://github.com/orgs/IT2901Nordic2024/discussions/1)

# Key terms

Below is a list of key terms in the project and their associated definitions.

## Device

The term device refers to the 12-sided dodecahedron created for this project utilizing the Nordic Semiconductor [Thingy:91 Cellular IoT prototyping platform.](https://www.nordicsemi.com/Products/Development-hardware/Nordic-Thingy-91)

## Habit

A user can configure and track up to 11 different habits at once. The 12th side of the dodecahedron is reserved for a "default state" where the user does not track any habit.
A user can choose a custom name for each habit and select a type of habit to track for each one.

A type refers to a pre-defined list of different habits that can be tracked, for instance a counter or a time-tracker.

In essence, this means that a habit is a combination of the user-configured name and the selected type.
The user's tracked data for each habit is stored in a database and the user can see a timeline of each habit visualized in the frontend as each time a habit is incremented the timestamp is also stored.

Even though the user can only track 11 habits on the device, they may still have more habits stored in the database and can still visualize them in the timeline. Additionally they can continue tracking a previous habit if needed by reconfiguring a side to track that habit.

## Timeline

The timeline refers to the frontend page where a user can see the tracked data of a habit over time.
This allows the user to either select one habit to see it over time or select several habits to compare them or find connections.
For instance a user might want to track how many push-ups they're doing. They would then configure it as a habit called "Push-ups" with the type set to "count". They can then see a visualization of how many push-ups they have done every day (once they have tracked them, of course) such as in the example image below.

![Example chart showing pushups over time](images/example_pushups.png)

When comparing two different habits, it may be natural to have different units on the y-axis, especially if the habits are of different type. That can be visualized like the example image below.

![Chart showing series A and series B with different y-axis units](images/example_different_y_axis.png)

The example images are from ApexCharts which is likely to be the library used for visualization of tracked habits.
The library also supports zooming in timeline charts which means the user can see habits for a specific day, week, month or whichever specific timeframe they wish.
