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
## 3.Aktörler
İlgili  kullanım durumunu gerçekleştirmeye yetkili olan kullanıcı sınıf(lar)ını belirtir..
  <a name="actors--name"></a><a name="3.1"></a>
  - [3.1](#actors--name) Tekil bir öz isim kullanın. Bu özelliği vurgulamak için, oyuncunun adını büyük harfle yazın.
    - Olumlu örnek: Spirit Team Direktörü *&lt;completes a task&gt;*.
    - Olumsuz örnek: Ruh takımı yönetmeni *&lt;completes a task&gt;*.

**[⬆ back to top](#table-of-contents)**

<a name="precondition"></a>
## 4.Ön Koşullar
Kullanım durumunun başlaması için gerekli olan başlangıç koşullarını tanımlamak için kullanılır.
   <a name="precondition"></a><a name="4.1"></a>
   - [4.1](#precondition) 
     
    - Positive example: The user must be logged into the system.
    
    - Negative example: The password reset link must not have expired.
    
The use cases that must be completed in the prerequisites should be specified.
         > Rationale: This is incredibly useful for software architecture design and UI design. E.g., "View a *&lt;whatever&gt;*" is related to "Find *&lt;whatever&gt;* s."

**[⬆ back to top](#table-of-contents)**

<a name="action-steps"></a>
## 5. Ana AKış
Kullanım durumunun normal, beklenen işlem adımlarını detaylandırmak için kullanılır. 

  <a name="action-steps--primary-actor-intention"></a><a name="6.1"></a>
  - [6.1](#action-steps--primary-actor-intention) Birincil Oyuncunun niyetini tanımlamak için aşağıdaki ifadeleri ve cümle yapısını kullanın :
    - The *&lt;Primary Actor&gt;* ... işaret eder/seçer/tercih eder/talep eder/denemeye çalışır.
    - The *&lt;Primary Actor&gt;* sunar . . .
    - The *&lt;Primary Actor&gt;* görünümler . . .
    - The *&lt;Primary Actor&gt;* doğrular . . . ve onaylar . . .
    - The *&lt;Primary Actor&gt;* girer/sağlar/belirtir . . . ve girmeyi bitirdiğini onaylar.
    - The *&lt;Primary Actor&gt;* girmeye devam ediyor. . .
    - The *&lt;Primary Actor&gt;* . . . bitirdiğini doğrulayana kadar . . .
    - The *&lt;Primary Actor&gt;* . . . (örneğin uyarıyı veya ikazı) kabul eder ve devam etmeyi onaylar.
    - The *&lt;Primary Actor&gt;* uyarıyı/alarmı yok sayar ve devam etmeyi onaylar.

  <a name="action-steps--user-feedback"></a><a name="6.6"></a>
  - [6.2](#action-steps--user-feedback) Kullanıcı her zaman Sistem’e geri bildirimde bulunur.
   - Olumlu örnek: Kullanıcı, . . .'nin tamamlandığını onaylar.
   - Olumlu örnek: Sistem . . .'yi işler ve Kullanıcıya . . .'yi gösterir, ardından Kullanıcı bu gösterimi kabul eder.

  <a name="action-steps--first-step"></a><a name="6.7"></a>
  - [6.3](#action-steps--first-step) Ana başarı senaryosundaki ilk cümle, kullanım durumunda açıklanan işlevselliğin yürütülmesini etkinleştiren olayı bildirmelidir.

  <a name="action-steps--end-step"></a><a name="6.8"></a>
  - [6.4](#action-steps--end-step) Bir kullanım örneğinin sonunu açıkça belirtmek için "Kullanım örneği sonlanır." ifadesini kullanın.

 

**[⬆ back to top](#table-of-contents)**


<a name="Alternative Streams"></a>
## 6.Alternatif Akış
Ana akışın dışında, belirli koşullarda devreye giren alternatif işlem yollarını açıklamak için kullanılır.
  <a name="extensions--syntax"></a><a name="7.1"></a>

  - [6.1](#alternative-streams) Uzantı koşulu iki nokta üst üste (:) noktalama işareti ve kalın yazıyla takip edilir:

- Olumlu örnek: **6a. Giriş doğrulama kuralı ihlali:**
- Olumsuz örnek: 6a. Giriş doğrulama kuralı ihlali.
- Olumsuz örnek: 6a. Giriş doğrulama kuralı ihlali

  - [6.2](#alternative-streams) Kullanım durumu uzantılarının işlenmesini tanımlamak için aşağıdaki ifadeleri ve cümle yapısını kullanın:

- Sistem, *&lt;Primary Actor&gt;*'a bir girdi doğrulama kuralının ihlal edildiğini bildirir ve hatanın niteliğini ve yerini görüntüler.
- *&lt;Primary Actor&gt;* hatayı düzeltir, ardından normal akışın . . . adımına döner.
- *&lt;Primary Actor&gt;* kullanım durumunu sonlandırmayı seçer.

  İşte bir uzantı koşulunun ve işleme adımlarının bir örneği:

**5a. Giriş doğrulama kuralı ihlali:**

​ 5a1. Sistem, Müşteriyi bir giriş doğrulama kuralının ihlal edildiği konusunda uyarır ve hatanın niteliğini ve yerini görüntüler.

​ 5a2. Müşteri hatayı düzeltir ve normal akışın 6. adımına döner.


**[⬆ back to top](#table-of-contents)**

<a name="last-condition"></a>
## 7. Exceptional Situation
An extension describes either an exception of a step in the main success scenario or an alternative success scenario.
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
Business rules include corporate policies, government regulations, laws, industry standards, and computational algorithms.
  <a name="business-rules--syntax"></a><a name="8.1"></a>
  - [8.1](#business-rules--syntax) Specify related business rules (e.g., security and access control requirements) in the business rules section:
    - Identify any relevant business rules concerning security/access.
    - Specify more finer-grained access control.
    - Specify any limitations regarding which individuals, groups, or organizations are permitted to initiate this use case or which data they are permitted to access.


<a name="notes"></a>
## 9. Notes
   
**[⬆ back to top](#table-of-contents)**
