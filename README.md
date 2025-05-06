# A Practical Style Guide and Templates Repository for Writing Effective Use Cases


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

<table style="width:100%; text-align: right;">
  <tr>
    <td>KD Tanımı</td>
    <td style="width:100%" colspan="3"></td>
  </tr>
  <tr>
    <td>Aktörler</td>
    <td style="width:100%" colspan="3"></td>
  </tr>
  <tr>
    <td>Ön Koşullar</td>
    <td style="width:100%" colspan="3"></td>
  </tr>
  </tr>
    <td>Ana Akış</td>
    <td style="width:100%" colspan="2"></td>
    <td></td>
  </tr>
  </tr>
    <td>Alternatif Akış</td>
    <td style="width:100%" colspan="3"></td>
  </tr>
  <td>İstisnai Durum</td>
    <td style="width:100%" colspan="3"></td>
  </tr>
   <td>İş Kuralları</td>
    <td style="width:100%" colspan="3"></td>
  </tr> 
   <td>Notlar</td>
    <td style="width:100%" colspan="3"></td>
  </tr> 

</table>

**[⬆ back to top](#table-of-contents)**

<a name="actors"></a>
## 3.Actor
An actor specifies a role played by a user or any other system that interacts with the system under development.
  <a name="actors--name"></a><a name="3.1"></a>
  - [3.1](#actors--name) Use a singular substantive name.
    - Positive example: Customer *&lt;completes a task&gt;*.
    - Negative example: The spirit team director *&lt;completes a task&gt;*.

**[⬆ back to top](#table-of-contents)**

<a name="precondition"></a>
## 4.Precondition
Preconditions: List what must be true before the use case starts.The preconditions that the user must fulfill in order to perform the action defined in the KD must be defined.The KDs that must be completed to complete this KD are listed at the bottom after the prerequisites.
<a name="precondition"></a><a name="4.1"></a>
- [4.1](#precondition)

- Preconditions example:
- The user must be logged into the system.
- The user must have selected the Application List from the menu.
- The following Use Cases must be completed.
     <p style="color:blue;">General.KD.3 Login to NDK System.</p>
     <p style="color:blue;"> NMSMİ.FG.5.KD.1 List Applications (5).</p>
**[⬆ back to top](#table-of-contents)**

<a name="action-steps"></a>
## 5.Action steps
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

  <a name="action-steps--user-feedback"></a><a name="6.6"></a>
  - [6.3](#action-steps--user-feedback) The User always provides feedback to the System.
    - Positive example: The User confirms that the . . . is complete.
    - Positive example: The System processes . . . and indicates to the User . . . , then the User acknowledges the indication.

  <a name="action-steps--first-step"></a><a name="6.7"></a>
  - [6.4](#action-steps--first-step) The first sentence in the main success scenario must report the event that activates the execution of the functionality described in the use case.

  <a name="action-steps--end-step"></a><a name="6.8"></a>
  - [6.5](#action-steps--end-step) Use "Use case ends." to explicitly indicate the end of a use case.

  <a name="action-steps--include-use-case"></a><a name="6.9"></a>
  - [6.6](#action-steps--include-use-case) When including another use case, use "The User or System *&lt;completes a task&gt;* through <ins>UC-*&lt;ID&gt;*: *&lt;Use Case Name&gt;*</ins>."
 

**[⬆ back to top](#table-of-contents)**


<a name="Alternative Streams"></a>
## 6.Alternative Flow
It is used to describe alternative processing paths outside the main flow that come into play under certain conditions.
<a name="extensions--syntax"></a><a name="7.1"></a>

- [6.1](#alternative-streams) The extension condition is followed by a colon (:) punctuation mark and boldface:

- Positive example: **6a. Input validation rule violation:**
- Negative example: 6a. Input validation rule violation.
- Negative example: 6a. Input validation rule violation

- [6.2](#alternative-streams) Use the following expressions and sentence structure to describe the processing of use case extensions:

- The system notifies *&lt;Primary Actor&gt;* that an input validation rule has been violated and displays the nature and location of the error.
- *&lt;Primary Actor&gt;* corrects the error, then returns to step . . . of the normal flow.
- *&lt;Primary Actor&gt;* chooses to terminate the use case.

Here is an example of an extension condition and processing steps:

**5a. Input validation rule violation:**

​ 5a1. The system warns the Client that an input validation rule has been violated and displays the nature and location of the error.

​ 5a2. The Client corrects the error and returns to step 6 of the normal flow.


**[⬆ back to top](#table-of-contents)**

<a name="last-condition"></a>
## 7. Exceptional Situation
It is used to explain the situations that cause the main flow to be interrupted unexpectedly and the actions to be taken in these situations. The Message Code in the table is used for Warning, Error, Notification messages.
  <a name="extensions--syntax"></a><a name="7.1"></a>

  - [7.1](#extensions--syntax) The extension condition is followed by the colon (:) punctuation and boldfaced:

    - Positive example: **6a. Input validation rule violation:**
    - Negative example: 6a. Input validation rule violation.
    - Negative example: 6a. Input validation rule violation

  - [7.2](#extensions--syntax) Use the following wording and sentence structure to describe the handling of use case extensions:

    - The System alerts the *&lt;Primary Actor&gt;* that an input validation rule is violated and displays the nature and location of the error.
    - The *&lt;Primary Actor&gt;* corrects the mistake, then returns to step . . . of the normal flow.
    - The *&lt;Primary Actor&gt;* chooses to terminate the use case.

    Here is an example of an extension condition and its handling steps:

    **6a. Input validation rule violation:**

    ​	6a1. The System alerts the Customer that an input validation rule is violated and displays the nature and location of the 	error.

    ​	6a2. The Customer corrects the mistake and returns to step 6 of the normal flow.

**[⬆ back to top](#table-of-contents)**

<a name="business-rules"></a>
## 8. Business rules
Used to define specific business rules that should be implemented within the scope of the use case.
  <a name="business-rules--syntax"></a><a name="8.1"></a>
  - [8.1](#business-rules--syntax) Specify related business rules (e.g., security and access control requirements) in the business rules section:
    - Identify any relevant business rules concerning security/access.
    - Specify more finer-grained access control.
    - Specify any limitations regarding which individuals, groups, or organizations are permitted to initiate this use case or which data they are permitted to access.


<a name="notes"></a>
## 9. Notes
Used to share additional information, explanations or details about the use case.
   
**[⬆ back to top](#table-of-contents)**
