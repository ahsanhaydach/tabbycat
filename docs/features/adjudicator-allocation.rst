.. _adjudicator-allocation:

======================
Adjudicator Allocation
======================

The adjudicator allocation screen offers the ability to automatically generate an allocation and/or allow you to create or edit an allocation manually. This interface is somewhat complex as it attempts to provide all of the information needed to inform allocation while also providing a number of automatic and manual tools for the allocation process itself.

Assigning Debate Priority
=========================

For tournaments with more than a few debates you generally want to begin the allocation process by applying a priority value to your debates. A debate's priority value is used by the automatic adjudicator allocator (or the preformed panel indicator) to match the strongest panels to the debates that need them most.

.. image:: images/allocation-prioritise.png

The prioritise button in the top-left allows you to assign a priority value automatically based on a debate's bracket or its 'liveness'. Remember that in early rounds there are usually not enough results for the liveness of each debate to be distinct and that Tabbycat measures liveness based on the sum of all live break categories — a debate can have more liveness points than it has teams if there are teams that are live in multiple categories.

.. note:: The automatic prioritiser never uses the 'highest' priority value so that you can easily use this to highlight the debates that need the strongest panels without needing to redistribute the priority of other debates.

Regardless of whether you automatically assign priority, there are sliders to the left of each team that can be used to manually specify priority. These are usually used to override the automatic priority of a debate if that matchup needs and especially strong/weak/mediocre panel for reasons that are not reflected in its bracket/liveness.

.. image:: images/allocation-slider.png

.. note:: If each debate's priority is the same, the automatic adjudicator will fall-back on using the debate's bracket as a substitute for priority. Thus, you can skip the prioritisation process (or only prioritise the most/least important debates) if you want a relatively even spread of panellists (e.g. during Round 1).

Automatic Adjudicator Allocation
================================

Once you are happy with your priorities you can begin assigning adjudicators. This also has an (optional) automatic process that will create panels for you. In creating these panels automatically, the allocator will:

- Avoid creating 'hard' conflicts (i.e. personal or institutional clashes) between adjudicators and teams while also trying to avoid 'soft' conflicts (i.e. avoiding an adjudicator seeing the same team again).
- Form panels whose relative average voting score matches the relative priority you assigned to each debate.
- Allocate trainees (unless disabled or none are under the threshold) to panels (allocated first to the highest-strength panels).
- Violate the above intents in cases where there are inescapable constraints — e.g. if there are too many soft or hard conflicts to avoid creating panels that do not trigger them.

.. note:: Remember that Tabbycat will only automatically allocate adjudicators that have been marked as available for this round.

To begin this process, click the *Allocate* button in the top-left. If you have :ref:`formed preformed panels <preformed-panels>`  for this round, the modal will first ask whether you want to assign adjudicators using those panels; otherwise the modal will contain a number of options that can be used to control the allocation. In general, the *minimum feedback score* value is the most important setting to consider as it determines the threshold needed for adjudicators to not be allocated as trainees.

.. image:: images/allocation-modal.png

Once you click *Auto-Allocate Adjudicators* the modal should disappear and your panels should appear. At large tournaments, and in the later rounds, it is not unheard of for this process to take a minute or longer.

.. note:: You can re-run the automatic allocation process on top of an existing allocation. Thus it is worth tweaking your priorities or allocation settings if the allocation does not seem optimal to you. Also note that the allocation process is not deterministic — if you rerun it the panels will be different.

Once your adjudicators have been allocated you can drag and drop them on to different panels. You can also drag and drop them to the 'unused area' (the gray bar at the bottom of the page) if you wish to store them temporarily or remove them from the draw. Dropping an adjudicator into the chair position will 'swap' that adjudicator into the previous position of the new chair.

Saving, Live Updates, and Sharing
=================================

Changes to your panels save automatically and you can exit the allocation page whenever you wish.

In addition, the allocation pages maintain a 'live' connection to the server that shows updates made by other users who are viewing/using the same page. That is to say, if two people on two computers are both viewing the allocation page they should see each other's changes in real-time. This allows you to 'distribute' the task of allocation across individual people (rather than sharing a screen/projector) if desired.

.. note:: It is possible to have users 'undo' or 'overwrite' each others changes despite this live system, e.g. if both users drag and adjudicator somewhere at the same time.

If you are dividing the task of allocation across multiple people, the *Sharding* system can help by allowing individuals to limit their view of the draw. The use case here is usually to divide the draw up into mutually-exclusive subsets so that individuals (or groups) of the adjudication core can focus on creating panels across the draw in parallel.

.. image:: images/allocation-sharding.png

To activate sharding, click the small icon to the right of the "Allocate" button. This then presents a number of options for how the draw is divide up into distinct sets. If you want to ensure that each person opens a completely distinct set of the draw, you will need to coordinate the options that each user selects here. They will need to set the **same** options for *Shard Mix*, *Shard Split* and *Shard Sort* but select a **different** *Open* option (i.e. opt-in to viewing a different shard from the other users). The ability to exit a sharded view is available in the same dialogue.

In-Place Highlights
===================

Adjudicators and teams may have borders of varying colors. These borders indicate that there is a clash — soft or hard — within a debate and highlights the teams/adjudicators that have triggered this. There is a key for these colors available at the top of the page — e.g. orange means *institutional conflict* while blue means *this adjudicator has seen this adjudicator/team before*.

.. image:: images/allocation-inplace.png

In general, you want to be on the lookout for red borders ('hard conflicts') and for teams with orange borders (institutional conflicts). Blue borders on teams/adjudicators and orange borders between adjudicators are usually of lesser concern.

.. note:: There are two 'special' types of highlight — a gray background in the chair position (no chair) or in the panellist position (the panel is not an odd-size). Adjudicators may also have a black background if they have not been marked as available.

Hover Highlights
================

When you hover over an adjudicator or team, they will take on a purple background and other adjudicators or teams may suddenly have different colored backgrounds. These indicate the conflicts that this team/adjudicator has with those other teams/adjudicators. By showing this information you can avoid swapping that adjudicator into a new debate which they have a conflict with.

.. image:: images/allocation-hovers.png

When you hover over an adjudicator or team the top-most area of the screen will show additional information about them, such as all of their previous institutions, their conflicts, their break category, their team members, their region, and who they saw in the last few rounds.

Toggle Highlights
=================

In the top-right of the interface are a number of toggles that changes the color of adjudicators and teams to more easily check specific types of information. For example, selecting the gender toggle will color-code teams and adjudicators with the gender that has been recorded in Tabbycat. Note that when a toggle is active, the color key will update to show the meaning of these new colors.

.. image:: images/allocation-highlights.png

.. note:: When finalising an adjudication you may want to ensure you have turned off any toggle highlights — often they make it more difficult to see the border colors that indicate conflicts.
