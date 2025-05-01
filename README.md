# A Practical Style Guide and Templates Repository for Writing Effective Use Cases

*An opinionated style guide for use case writing*

Software developers are most effective when handed with a set of consistent and self-contained use cases. However, writing high-quality use cases is a difficult and time-consuming task. Inspired by the success of various coding style guides, we developed a use case writing style guide and a small set of use case templates to slightly constrain the way a use case is written. This style guide will help reduce excessive personal idiosyncrasy in use case writing and give a uniform appearance to the use case written by different requirements engineers so that it is much easier to understand a large set of use cases. 

Instead of overly restricting the use case writing process, the purpose of this style guide is to find a balance between readability and creativity.

> **Note**: The use case templates repository is available at [here](./use-case-templates/README.md). A real project's use case specification following this style guide is available at [here](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit?usp=sharing). Feel free to provide feedback.

## Table of contents

1. [Generic use case specification format](#generic-use-case-specification-format)
2. [Use case naming](#use-case-naming)
3. [Actors](#actors)
4. [Precondition](#precondition)
5. [Action steps](#action-steps)
6. [Alternative Streams](#alternative-streams)
7. [Last Condition](#last-condition)
8. [Business rules](#business-rules)
9. [Information Assets](#information-assets)

<a name="generic-use-case-specification-format"></a>
## 1. Generic use case specification format

<a name="generic-use-case-specification-format--syntax"></a><a name="1.1"></a>

  - [1.1](#generic-use-case-specification-format--syntax) We adopt the use case specification format from [Software Requirements (Third Edition)](https://www.microsoftpressstore.com/store/software-requirements-9780735679665) by Karl Wiegers and Joy Beatty with slight modification as a basis for writing use cases.
<table style="width:100%; text-align: right;">
  <tr>
    <td>KD Kodu</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>KD Tanımı</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Aktörler</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Ön Koşul</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
    <td rowspan="4">Ana Akış</td>
    <td style="width:60%" colspan="2">Kullanıcı</td>
    <td>Sistem</td>
  </tr>
  </tr>
    <td style="width:60%" colspan="2">&emsp;</td>
    <td rowspan="3"></td>
  </tr>
  </tr>
    <td style="width:60%" colspan="2">&emsp;</td>
  </tr>
  </tr>
    <td style="width:60%" colspan="2">&emsp;</td>
  </tr>
  </tr>
    <td>Alternatif Akışlar</td>
    <td style="width:60%" colspan="2"></td>
    <td></td>
  </tr>
  </tr>
    <td>İş Kuralları</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  </tr>
    <td rowspan="2">Bilgi Varlıkları</td>
    <td style="width:60%" colspan="2">Birinci Seviye</td>
    <td>İkinci Seviye</td>
  </tr>
  <tr>
    <td colspan="2">&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</td>
    <td>&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</td>
  </tr>
</table>




**[⬆ back to top](#table-of-contents)**

<a name="use-case-naming"></a>
## 2. Use case naming
  <a name="use-case-naming--id"></a><a name="2.1"></a>
  - [2.1](#use-case-naming--id) Assign a unique ID to each use case.
    > Rationale: This ensures that you can quickly identify one use case.

  <a name="use-case-naming--verb"></a><a name="2.2"></a>
  - [2.2](#use-case-naming--verb) Start with a verb with the first letter capitalized and describe the goal of the user.
    - Positive example: NİV.FG.2.KD.1: Request a SuperFrog appearance for TCU events
    - Negative example: SuperFrog appearance request management

**[⬆ back to top](#table-of-contents)**

<a name="actors"></a>
## 3. Actors
An actor specifies a role played by a user or any other system that interacts with the system under development. 
  <a name="actors--name"></a><a name="3.1"></a>
  - [3.1](#actors--name) Use a singular substantive name. To highlight this characteristic, capitalize the actor's name.
    - Positive example: The Spirit Team Director *&lt;completes a task&gt;*.
    - Negative example: The spirit team director *&lt;completes a task&gt;*.

**[⬆ back to top](#table-of-contents)**

<a name="precondition"></a>
## 4.Precondition
Used to define the initial conditions required for the use case to start.If these conditions are not met, the use case cannot be executed or the expected outputs cannot be obtained.
   <a name="precondition"></a><a name="4.1"></a>
   - [4.1](#precondition) Use a singular substantive name. To highlight this characteristic, capitalize the actor's name.
     
    - Positive example: The user must be logged into the system.
    
    - Negative example: The password reset link must not have expired.
    
The use cases that must be completed in the prerequisites should be specified.
         > Rationale: This is incredibly useful for software architecture design and UI design. E.g., "View a *&lt;whatever&gt;*" is related to "Find *&lt;whatever&gt;* s."

**[⬆ back to top](#table-of-contents)**

<a name="action-steps"></a>
## 5. Action steps
Use case action steps are sentences that form a use case's main success scenario and extensions. According to [Alistair Cockburn](https://g.co/kgs/Hy777n), a use case action step either describes an interaction between two actors e.g., "The Customer enters address information." or a validation step to protect interest of a stakeholder e.g., "The System validates the credentials." or an internal change to satisfy a stakeholder e.g., "The System deducts amount from balance." Our style guide complements Cockburn's classic 10 action step writing guidelines by recommending proper words and sentence structures.

  <a name="action-steps--primary-actor-intention"></a><a name="6.1"></a>
  - [6.1](#action-steps--primary-actor-intention) Use the following wording and sentence structure to describe the Primary Actor's intention (Corresponds to Cockburn's interaction between two actors):
    - The *&lt;Primary Actor&gt;* indicates to/selects to/chooses to/requests to/attempts to . . .
    - The *&lt;Primary Actor&gt;* submits . . .
    - The *&lt;Primary Actor&gt;* views . . .
    - The *&lt;Primary Actor&gt;* verifies . . . and confirms . . .
    - The *&lt;Primary Actor&gt;* enters/provides/specifies . . . and confirms that she has finished entering.
    - The *&lt;Primary Actor&gt;* continues entering . . .
    - The *&lt;Primary Actor&gt;* . . . until she confirms that she has finished . . .
    - The *&lt;Primary Actor&gt;* acknowledges . . . (e.g., the alert or warning) and confirms to continue.
    - The *&lt;Primary Actor&gt;* ignores the warning/alarm and confirms to continue.

  <a name="action-steps--systen-internal-processing"></a><a name="6.2"></a>
  - [6.2](#action-steps--systen-internal-processing) Use the following wording and sentence structure to describe the system internal processing (Corresponds to Cockburn's validation step and internal change):
    - The System validates, saves, records, calculates, updates, deletes, creates, retrieves, triggers . . .

  <a name="action-steps--system-interaction"></a><a name="6.3"></a>
  - [6.3](#action-steps--system-interaction) Use the following wording and sentence structure to describe an interaction started by the System (Corresponds to Cockburn's interaction between two actors):
    - The System displays/shows/presents/informs . . . according to . . . defined in the Associated Information of this use case. (This is usually the information retrieved from a data source. For example, a list of products or a graph of stats. The previous action step may be "The System retrieves . . . ".)
    - The System alerts/warns/alarms . . . (This is used when something is about to break the business rule, or something is about the change the state of the system, usually occurs in extensions.)
    - The System asks the *&lt;Primary Actor&gt;* to enter . . . according to . . . defined in the Associated Information of this use case.
    - The System prompts the *&lt;Primary Actor&gt;* . . . (The system knows some information that would help the user decide what to do next) or The System offers . . . options/methods/choices . . .
    - The System notifies/sends *&lt;Secondary Actors&gt;* . . .

  <a name="action-steps--system-to-system-interaction"></a><a name="6.4"></a>
  - [6.4](#action-steps--system-to-system-interaction) Use the following wording and sentence structure to describe an interaction between the System and another system in the environment (Corresponds to Cockburn's interaction between two actors):
    - The System has another system do something.
    - The System requests another system to do something.
    - Another System provides . . .

  <a name="action-steps--system-feedback"></a><a name="6.5"></a>
  - [6.5](#action-steps--system-feedback) The System always provides feedback that the requested task has been finished. This allows the User to know the command has been completed, even if it is not immediately obvious.
    - Positive example: The System indicates that the calculation is finished.

  <a name="action-steps--user-feedback"></a><a name="6.6"></a>
  - [6.6](#action-steps--user-feedback) The User always provides feedback to the System.
    - Positive example: The User confirms that the . . . is complete.
    - Positive example: The System processes . . . and indicates to the User . . . , then the User acknowledges the indication.

  <a name="action-steps--first-step"></a><a name="6.7"></a>
  - [6.7](#action-steps--first-step) The first sentence in the main success scenario must report the event that activates the execution of the functionality described in the use case.

  <a name="action-steps--end-step"></a><a name="6.8"></a>
  - [6.8](#action-steps--end-step) Use "Use case ends." to explicitly indicate the end of a use case.

  <a name="action-steps--include-use-case"></a><a name="6.9"></a>
  - [6.9](#action-steps--include-use-case) When including another use case, use "The User or System *&lt;completes a task&gt;* through <ins>UC-*&lt;ID&gt;*: *&lt;Use Case Name&gt;*</ins>."

**[⬆ back to top](#table-of-contents)**


<a name="Alternative Streams"></a>
## 6.Alternative Streams
It is used to describe alternative processing paths outside the main flow that come into play under certain conditions.
  <a name="extensions--syntax"></a><a name="7.1"></a>

  - [6.1](#alternative-streams) The extension condition is followed by the colon (:) punctuation and boldfaced:

    - Positive example: **6a. Input validation rule violation:**
    - Negative example: 6a. Input validation rule violation.
    - Negative example: 6a. Input validation rule violation

  - [6.2](#alternative-streams) Use the following wording and sentence structure to describe the handling of use case extensions:

    - The System alerts the *&lt;Primary Actor&gt;* that an input validation rule is violated and displays the nature and location of the error.
    - The *&lt;Primary Actor&gt;* corrects the mistake, then returns to step . . . of the normal flow.
    - The *&lt;Primary Actor&gt;* chooses to terminate the use case.

    Here is an example of an extension condition and its handling steps:

    **5a. Input validation rule violation:**

    ​	5a1. The System alerts the Customer that an input validation rule is violated and displays the nature and location of the 	error.

    ​	5a2. The Customer corrects the mistake and returns to step 6 of the normal flow.


<a name="business-rules"></a>
## 7. Business rules
Business rules include corporate policies, government regulations, laws, industry standards, and computational algorithms.
  <a name="business-rules--syntax"></a><a name="7.1"></a>
  - [7.1](#business-rules--syntax) Specify related business rules (e.g., security and access control requirements) in the business rules section:
    - Identify any relevant business rules concerning security/access.
    - Specify more finer-grained access control.
    - Specify any limitations regarding which individuals, groups, or organizations are permitted to initiate this use case or which data they are permitted to access.

**[⬆ back to top](#table-of-contents)**

<a name="last-condition"></a>
## 8. Post Condition
A postcondition for a use case lists the possible states that the system can be in after the use case runs. The system must be in one of these states. A postcondition also specifies the actions that the system takes at the end of the use case, regardless of what happens in the use case.
  <a name="post-condition"></a><a name="8.1"></a>
  - [8.1](#post-condition) Use a singular substantive name. To highlight this characteristic, capitalize the actor's name.
    - Positive example: The system connects the new leave request to the database and the request status is assigned as "Pending". The system sends an automatic notification to notify the administrator.
    - Negative example: The request cannot be created. The system does not save any data, the current error message is displayed, and the user remains on the form page.
  <a name="related-use-cases--required"></a><a name="10.1"></a>
  - [10.1](#related-use-cases--required) Provide related use cases.
    > Rationale: This is incredibly useful for software architecture design and UI design. E.g., "View a *&lt;whatever&gt;*" is related to "Find *&lt;whatever&gt;* s."


**[⬆ back to top](#table-of-contents)**

<a name="information-assets"></a>
## 9. Information Assets
Information assets are used to accurately define the data processed by the system in use cases, operations associated with user roles, and security requirements.
  <a name="first-level"></a><a name="9.1"></a>
  - [9.1](#first-level) First Level represents the main information entities used in the system (for example: User, Product, Order) and shows which main data entities the use cases are associated with.

  <a name="second-level"></a><a name="3.4"></a>
  - [9.2](#second-level) The Second Level specifies sub-data or properties of these main information entities (for example: User Types, User Information) and specifies the data details processed in the use cases.
   
**[⬆ back to top](#table-of-contents)**
