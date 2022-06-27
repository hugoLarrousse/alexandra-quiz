<!-- <template>
  <div class="">
    Hello
    <div>
      <div> Question 1</div>
      <div :class="questions[0].answer === 'y' && 'clicked'" @click="updateAnswer(0, 'y')">
        Yes
      </div>

      <div :class="questions[0].answer === 'n' && 'clicked'" @click="updateAnswer(0, 'n')">
        No
      </div>
      <button @click="submit">
        SUBMIT
      </button>
    </div>
  </div>
</template> -->

<template>
  <div>
    <div>
      <img id="banner" src="~/assets/banner2.png">
    </div>

    <div class="introduction">
      <p>
        Tout le monde mérite d'être dans une relation sûre et saine.<br>
        Sais-tu si c’est le cas de ta relation ? Réponds par oui ou par non aux questions suivantes pour le découvrir.
      </p>
    </div>

    <div class="questions">
      <!-- FIRST QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            1.
          </div>
          <div class="questioncontent">
            Au début de ta relation, tu étais comblé(e) d’amour et d’un coup, ça s’est arrêté.<br><br>
            <div :class="questions[0].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(0,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[0].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(0,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- SECOND QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            2.
          </div>
          <div class="questioncontent">
            Ta relation se caractérise en grande partie par des disputes, du stress et des reproches.<br><br>
            <div :class="questions[1].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(1,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[1].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(1,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- THIRD QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            3.
          </div>
          <div class="questioncontent">
            Il/elle n’arrête pas de te rabaisser sans raison.<br><br>
            <div :class="questions[2].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(2,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[2].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(2,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- FOURTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            4.
          </div>
          <div class="questioncontent">
            Ta relation connaît énormément de hauts et de bas. C’est soit le bonheur pur, soit l’horreur.<br><br>
            <div :class="questions[3].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(3,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[3].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(3,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- FIFTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            5.
          </div>
          <div class="questioncontent">
            Tu as l’impression de toujours donner et de ne rien recevoir en retour.<br><br>
            <div :class="questions[4].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(4,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[4].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(4,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- SIXTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            6.
          </div>
          <div class="questioncontent">
            Ton partenaire ne s’excuse jamais après une dispute ou n’a jamais reconnu ses propres erreurs.<br><br>
            <div :class="questions[5].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(5,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[5].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(5,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- SEVENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            7.
          </div>
          <div class="questioncontent">
            Quand il y a dispute, il/elle n’essaie même pas de te comprendre.<br><br>
            <div :class="questions[6].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(6,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[6].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(6,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- EIGHTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            8.
          </div>
          <div class="questioncontent">
            Tu vois de moins en moins tes amis ou ta famille parce qu’il/elle te l’interdit.<br><br>
            <div :class="questions[7].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(7,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[7].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(7,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- NINETH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            9.
          </div>
          <div class="questioncontent">
            Il/elle te rabaisse en public.<br><br>
            <div :class="questions[8].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(8,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[8].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(8,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- TENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            10.
          </div>
          <div class="questioncontent">
            Tu n’es pas heureux/heureuse, mais tu n’imagines pas mettre fin à cette relation.<br><br>
            <div :class="questions[9].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(9,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[9].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(9,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- ELEVENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            11.
          </div>
          <div class="questioncontent">
            Tu as l'impression que quoi que tu fasses, ce n'est jamais assez bien pour cette personne.<br><br>
            <div :class="questions[10].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(10,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[10].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(10,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- TWELVETH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            12.
          </div>
          <div class="questioncontent">
            Tu te sens fatigué, vidé de ton énergie quand tu passes du temps avec lui/elle.<br><br>
            <div :class="questions[11].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(11,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[11].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(11,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- THIRTEEN QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            13.
          </div>
          <div class="questioncontent">
            Tu as l’impression de marcher sur des œufs en permanence avec cette personne. Tu as peur qu’elle te rejette
            si tu ne fais pas comme elle veut.<br><br>
            <div :class="questions[12].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(12,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[12].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(12,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- FOURTEENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            14.
          </div>
          <div class="questioncontent">
            Tu te sens critiqué, dévalorisé ou jugé en permanence dans ta relation.<br><br>
            <div :class="questions[13].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(13,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[13].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(13,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- FIFTEENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            15.
          </div>
          <div class="questioncontent">
            Tu subis de cette personne des agressions psychologiques ou physiques régulièrement.<br><br>
            <div :class="questions[14].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(14,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[14].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(14,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- SIXTEENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            16.
          </div>
          <div class="questioncontent">
            Tu as la sensation que cette relation est abusive voire destructrice pour toi.<br><br>
            <div :class="questions[15].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(15,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[15].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(15,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- SEVENTEENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            17.
          </div>
          <div class="questioncontent">
            Tu as peur d’affirmer tes choix de vie, d’être pleinement toi-même avec lui/elle.<br><br>
            <div :class="questions[16].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(16,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[16].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(16,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- EIGHTEENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            18.
          </div>
          <div class="questioncontent">
            Tu as peur qu’il/elle arrête de t’aimer ou de te respecter s’il/elle te connaissait vraiment.<br><br>
            <div :class="questions[17].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(17,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[17].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(17,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- NINETEENTH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            19.
          </div>
          <div class="questioncontent">
            Tu as peur d'être en désaccord avec lui/elle.<br><br>
            <div :class="questions[18].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(18,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[18].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(18,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- TWENTIETH QUESTION -->
      <div class="question">
        <div class="toflex">
          <div class="questionnumber bold">
            20.
          </div>
          <div class="questioncontent">
            Tu entretiens l'espoir qu'un jour cette personne change.<br><br>
            <div :class="questions[19].answer === 'y' && 'clicked'" class="yesorno" @click="updateAnswer(19,'y')">
              <div class="firstletter">
                O
              </div>
              <div class="answer">
                Oui
              </div>
            </div>
            <div :class="questions[19].answer === 'n' && 'clicked'" class="yesorno" @click="updateAnswer(19,'n')">
              <div class="firstletter">
                N
              </div>
              <div class="answer">
                Non
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="datas">
      <input id="name" v-model="name" type="text" name="name" placeholder="Ton prénom"><br>
      <input id="email" v-model="email" type="email" name="email" placeholder="Ton adresse mail"><br>
      <button class="submit" @click="submit">
        Voir le résultat
      </button>
    </div>

    <!-- FROM 0 TO 3 YES -->
    <div v-show="result <= 3" id="results1" class="results">
      <h2>Tu es dans une relation harmonieuse.</h2><br>
      <p>
        Ta relation ne présente pas ou très peu de critères de toxicité. Ta relation est harmonieuse, positive ou au
        minimum neutre.
      </p><br>
      <p>
        Mais si tu as réalisé ce test, c’est sûrement que tu n’es pas à l'aise dans cette relation, que certains de ses
        aspects te posent problème, qu’il y a des choses désagréables ou qui te dérangent.
      </p><br>
      <p>
        Ce test n'est qu'un indicatif, un repère pour évaluer si ta relation est toxique ou pas. Mais l’élément le plus
        important, celui à prendre en compte, c’est ton ressenti. C’est toi l’expert, écoute-toi, écoute ce que tu
        ressens, ton intuition. Tu as déjà une bonne partie des réponses.
      </p><br>
      <p>Si malgré ce résultat tu sens que :</p><br>
      <ul>
        <li>Cette relation n'est pas saine,</li>
        <li>Tu ne te sens pas à l’aise, ni toi-même,</li>
        <li>Tu ressens que quelque chose cloche,</li>
        <li>Tu ne te sens pas en confiance,</li>
        <li>Etc.</li>
      </ul><br>
      <p>
        Alors ça vaut peut-être le coup d'aller un peu plus loin dans la recherche de compréhension. Tu as déjà fait le
        premier pas. Apprendre à s'écouter et à respecter ses ressentis est la première étape.
      </p><br>
      <p>
        Pour aller plus loin, tu peux consulter les différents contenus de mes réseaux sociaux et t’abonner à La Lettre
        Rose, la newsletter qui t'accompagne dans tes relations.✨
      </p><br>
      <p>Je te partage chaque jeudi des conseils exclusifs pour améliorer tes relations et la maintenir saine.</p><br>
      <p>Si tu souhaites que l’on échange de manière plus personnelle, tu peux aussi prendre rendez-vous ! </p><br>
    </div>

    <!-- FROM 3 TO 6 YES -->
    <div v-show="result > 3 && result <= 6" id="results2" class="results">
      <h2>Tu es dans une relation légèrement toxique.</h2><br>
      <p>
        Ta relation présente quelques caractères toxiques. À partir de maintenant, augmente ta vigilance et veille à ce
        qu'elle ne bascule dans une toxicité plus importante.
      </p><br>
      <p>
        Mais si tu as réalisé ce test, c’est sûrement que tu n’es pas à l'aise dans cette relation, que certains de ses
        aspects te posent problème, qu’il y a des choses désagréables ou qui te dérangent.
      </p><br>
      <p>
        Ce test n'est qu'un indicatif, un repère pour évaluer si ta relation est toxique ou pas. Mais l’élément le plus
        important, celui à prendre en compte, c’est ton ressenti. C’est toi l’expert, écoute-toi, écoute ce que tu
        ressens, ton intuition. Tu as déjà une bonne partie des réponses.
      </p><br>
      <p>Si malgré ce résultat tu sens que :</p><br>
      <ul>
        <li>Cette relation n'est pas saine,</li>
        <li>Tu ne te sens pas à l’aise, ni toi-même,</li>
        <li>Tu ressens que quelque chose cloche,</li>
        <li>Tu ne te sens pas en confiance,</li>
        <li>Un rapport de force discret s’est installé,</li>
        <li>Tu te sens fatiguée par cette relation,</li>
        <li>Etc.</li>
      </ul><br>
      <p>
        Alors ça vaut peut-être le coup d'aller un peu plus loin dans la recherche de compréhension. Tu as déjà fait le
        premier pas. Apprendre à s'écouter et à respecter ses ressentis est la première étape.
      </p><br>
      <p>
        Pour aller plus loin, tu peux consulter les différents contenus de mes réseaux sociaux et t’abonner à La Lettre
        Rose, la newsletter qui t'accompagne dans tes relations.✨
      </p><br>
      <p>
        Je te partage chaque jeudi des conseils exclusifs pour améliorer tes relations. Et si tu veux aller encore plus
        loin, on peut échanger ensemble. Prends rendez-vous !
      </p><br>
    </div>

    <!-- FROM 6 to 14 YES -->
    <div v-show="result > 6 && result <= 14" id="results3" class="results">
      <h2>Tu es dans une relation très fortement toxique.</h2><br>
      <p>
        Ta relation présente un très grand nombre de critères de toxicité. Elle peut être considérée comme très
        fortement toxique.
      </p><br>
      <p>
        Il y a urgence à réagir et à te préserver à partir de maintenant. Prends certaines dispositions pour te
        protéger et éviter que ta relation ne bascule vers une toxicité encore plus importante. Si c’est le cas, elle
        deviendra franchement dangereuse pour ton équilibre physique et psychique. Et il sera plus difficile pour toi de
        t’en libérer. Alors n’attends plus…
      </p><br>
      <p>
        Si tu as réalisé ce test, il est probable que vous ayez déjà beaucoup souffert de cette Relation, qu'il y ait
        déjà eu de très nombreuses alertes internes, et peut-être même de votre entourage, que vous subissiez de
        nombreux aspects de cette relation, que vous soyez régulièrement blessé(e) émotionnellement voir que vous
        subissiez régulièrement différentes formes de violences et notamment des violences psychologiques.
      </p><br>
      <p>
        Ce test n'est qu'un indicatif, un repère pour évaluer si ta relation est toxique ou pas. Mais avec de tels
        résultats, il est évident que cette relation est un poison pour toi. Elle ne te fait pas du bien. Tu es très
        éloigné d'une relation positive et harmonieuse… Dans ton cas, la relation est devenue malsaine et te fait
        probablement beaucoup de mal… Je me trompe ?
      </p><br>
      <p>
        L’élément le plus important, celui à prendre en compte, c’est ton ressenti. C’est toi l’expert, écoute-toi,
        écoute ce que tu ressens, ton intuition. Tu as déjà une bonne partie des réponses. Tu sais probablement que
        cette relation n'est pas saine pour toi et qu’elle te fait du mal.
      </p><br>
      <p>Tu as la sensation que :</p><br>
      <ul>
        <li>Cette relation n'est pas saine,</li>
        <li>Tu ne te sens pas à l’aise, ni toi-même,</li>
        <li>Tu ressens que quelque chose cloche</li>
        <li>Tu ne te sens pas en confiance</li>
        <li>Un rapport de force discret s’est installé,</li>
        <li>Tu te sens épuisé, vidé par cette relation,</li>
        <li>Les limites ne sont pas claires,</li>
        <li>Etc.</li>
      </ul><br>
      <p>
        Alors ça vaut peut-être le coup d'aller un peu plus loin dans la recherche de compréhension. Tu as déjà fait le
        premier pas. Apprendre à s'écouter et à respecter ses ressentis est la première étape. Mais dans ton cas, cela
        ne suffit pas. Il est important que tu comprennes comment cette toxicité est apparue. Cela te permettra d’y
        apporter des réponses adaptées. Quand on est dans une relation toxique, on a souvent besoin d'aide, d'outils et
        de réponses rapides pour s'en protéger et en sortir.
      </p><br>
      <p>
        Je te propose de consulter les différents contenus de mes réseaux sociaux et t’abonner à La Lettre Rose, la
        newsletter qui t'accompagne dans tes relations.✨ Je te partage chaque jeudi des conseils exclusifs pour
        améliorer tes relations.
      </p><br>
      <p>Si tu ressens une urgence à te sortir de ta relation, tu peux directement prendre rendez-vous avec moi.</p><br>
    </div>

    <!-- FROM 14 to 20 YES -->
    <div v-show="result > 14" id="results4" class="results">
      <h2>Tu es dans une relation extrêmement toxique. Cette relation est considérée comme dangereuse.</h2><br>
      <p>
        Ta relation présente tellement de critères de toxicité qu'elle peut être considérée comme extrêmement toxique,
        voire dangereuse. Il y a urgence ! Tu dois réagir et à te préserver dès maintenant. Prends certaines
        dispositions pour te protéger, pour éviter d'y laisser ta peau, ta santé physique et psychique et démarre un
        chemin pour te libérer rapidement de cette relation.
      </p><br>
      <p>
        Si tu as réalisé ce test, c’est que tu es déjà en grande souffrance dans ta relation. Tu as surement déjà eu de
        très nombreuses alertes internes, et peut-être même de ton entourage. Tu subis certainement de nombreux aspects
        de cette relation, que vous soyez régulièrement blessé(e) émotionnellement voir que vous subissiez régulièrement
        différentes formes de violences et notamment des violences psychologiques.il est probable que vous ayez déjà
        beaucoup souffert de cette Relation, qu'il y ait déjà eu de très nombreuses alertes internes, et peut-être même
        de votre entourage, que vous subissiez de nombreux aspects de cette relation, que vous soyez régulièrement
        blessé(e) émotionnellement voir que vous subissiez régulièrement différentes formes de violences et notamment
        des violences psychologiques.
      </p><br>
      <p>
        Ce test n'est qu'un indicatif, un repère pour évaluer si ta relation est toxique ou pas. Mais avec de tels
        résultats, il est évident que cette relation est un poison pour toi. Elle te fait beaucoup de mal. C’est
        clairement l’opposé d'une relation positive et harmonieuse… Dans ton cas, la relation est devenue malsaine et te
        détruis à petit feu… Je me trompe ?
      </p><br>
      <p>
        L’élément le plus important, celui à prendre en compte, c’est ton ressenti. C’est toi l’expert, écoute-toi,
        écoute ce que tu ressens, ton intuition. Tu as déjà une bonne partie des réponses. Tu sais probablement que
        cette relation n'est pas saine pour toi et qu’elle te fait du mal.
      </p><br>
      <p>Tu as la sensation que :</p><br>
      <ul>
        <li>Cette relation n'est pas saine,</li>
        <li>Tu ne te sens pas à l’aise, ni toi-même,</li>
        <li>Tu ressens que quelque chose cloche</li>
        <li>Tu ne te sens pas en confiance</li>
        <li>Un rapport de force discret s’est installé,</li>
        <li>Tu te sens épuisé, vidé par cette relation,</li>
        <li>Les limites ne sont pas claires,</li>
        <li>Etc.</li>
      </ul><br>
      <p>
        Alors ça vaut peut-être le coup d'aller un peu plus loin dans la recherche de compréhension. Tu as déjà fait le
        premier pas. Apprendre à s'écouter et à respecter ses ressentis est la première étape. Mais dans ton cas, cela
        ne suffit pas. Il est important que tu comprennes comment cette toxicité est apparue. Cela te permettra d’y
        apporter des réponses adaptées. Quand on est dans une relation toxique, on a souvent besoin d'aide, d'outils et
        de réponses rapides pour s'en protéger et en sortir.
      </p><br>
      <p>Si tu ressens une urgence à te sortir de ta relation, tu peux directement prendre rendez-vous avec moi.</p><br>
      <p>
        Je te propose aussi de consulter les différents contenus de mes réseaux sociaux et t’abonner à La Lettre Rose,
        la newsletter qui t'accompagne dans tes relations.✨
      </p><br>
      <p>Je te partage chaque jeudi des conseils exclusifs pour améliorer tes relations.</p><br>
    </div>

    <div class="introduction">
      <h1>Qui suis-je ?</h1><br>
      <p>
        Salut, je suis Alexandra.🌸 <br><br>

        <img id="alexandra" src="alexandra.png">

        Mon objectif ? T’accompagner vers une relation plus saine et consciente. <br><br>

        Je t'aide à retrouver confiance en toi et à comprendre pourquoi ta relation est en péril. Ensemble,
        déconstruisons les croyances qui t’empêchent de t’épanouir pleinement.<br><br>

        Mes expériences de vies et professionnelles ainsi que ma formation en coaching, me permettent de t'apporter
        toutes les clés pour que tu t'épanouisses pleinement dans tes relations et que tu sois enfin toi-même !
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainComponent',
  data () {
    return {
      // 20 questions
      questions: [{
        id: 1,
        answer: '',
        question: ''
      }, {
        id: 2,
        answer: '',
        question: ''
      },
      {
        id: 3,
        answer: '',
        question: ''
      },
      {
        id: 4,
        answer: '',
        question: ''
      },
      {
        id: 5,
        answer: '',
        question: ''
      },
      {
        id: 6,
        answer: '',
        question: ''
      },
      {
        id: 7,
        answer: '',
        question: ''
      },
      {
        id: 8,
        answer: '',
        question: ''
      },
      {
        id: 9,
        answer: '',
        question: ''
      },
      {
        id: 10,
        answer: '',
        question: ''
      },
      {
        id: 11,
        answer: '',
        question: ''
      },
      {
        id: 12,
        answer: '',
        question: ''
      },
      {
        id: 13,
        answer: '',
        question: ''
      },
      {
        id: 14,
        answer: '',
        question: ''
      },
      {
        id: 15,
        answer: '',
        question: ''
      },
      {
        id: 16,
        answer: '',
        question: ''
      },
      {
        id: 17,
        answer: '',
        question: ''
      },
      {
        id: 18,
        answer: '',
        question: ''
      },
      {
        id: 19,
        answer: '',
        question: ''
      },
      {
        id: 20,
        answer: '',
        question: ''
      }],
      email: '',
      name: '',
      result: undefined,
      isAlreadySent: false
    }
  },
  computed: {
    // get all answered questions
    isAllAnswered () {
      return this.questions.every(question => question.answer)
    },
    // get how many yes answers
    yesAnswers () {
      return this.questions.filter(question => question.answer === 'y').length
    }
  },
  methods: {
    // check if there was already an answer
    updateAnswer (index, answer) {
      this.questions[index].answer = answer
    },
    // check if all questions are answered and show result
    validEmail (email) {
      return /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/.test(email)
    },
    submit () {
      if (!this.email || !this.name) {
        alert('Pense à remplir ton nom et ton email :)')
        return
      }
      if (!this.validEmail(this.email)) {
        alert('Attention, ton email semble invalide')
        return
      }

      if (!this.isAllAnswered) {
        alert('Pense à répondre à toutes les questions :)')
        return
      }

      const myHeaders = new Headers()
      myHeaders.append('Content-Type', 'application/json')

      const urlencoded = new URLSearchParams()

      urlencoded.append('value1', this.email)
      urlencoded.append('value2', this.name)
      urlencoded.append('value3', this.yesAnswers)

      const requestOptions = {
        method: 'POST',
        headers: myHeaders,
        body: urlencoded,
        mode: 'no-cors'
      }

      this.result = this.yesAnswers
      // location.hash = '#results'
      if (!this.isAlreadySent) {
        fetch('https://maker.ifttt.com/trigger/form_submitted/with/key/dHtIWuEacFEAbYgjhDgYl2nhuu2khaECxbyii4JUwaN', requestOptions).then(() => {
          this.isAlreadySent = true
          if (this.result <= 3) {
            location.hash = '#results1'
          } else if (this.result <= 6) {
            location.hash = '#results2'
          } else if (this.result <= 14) {
            location.hash = '#results3'
          } else {
            location.hash = '#results4'
          }
        })
      }
    }
  }

}
</script>

<style>
:root {
    --maincolor: #FEE3EC;
    --secondcolor: #F9C5D5;
    --thirdcolor: #F999B7;
    --fourthcolor: #F2789F;
    --fifthcolor: #A624DB;
}

html {
    scroll-behavior: smooth;
}

*{
    box-sizing: border-box;
    border: 0;
    margin: 0;
}
body {
    background-color: var(--maincolor);
    font-family: "Lato", sans-serif;
}
#banner {
    width: 100%;
}

.introduction {
    text-align: center;
    margin: 20px 10px;
    padding: 20px;
    border-radius: 5px;
    background-color: var(--secondcolor);
}

.toflex {
    display: flex;
    gap: 10px;
    margin: 20px;
}

.bold {
    font-weight: bold;
}

/* .questionnumber {
  width: 25px;
} */

.questioncontent {
    display: flex;
    flex-direction: column;
    gap: 5px;
}

.yesorno {
    background-color: var(--thirdcolor);
    border-radius: 6px;
    border: 1px solid var(--fourthcolor);
    display: flex;
    justify-content: left;
    align-items: center;
    gap: 8px;
    padding: 4px;
    width: 168px;
    height: 30px;
}

.yesorno:hover {
    background-color: var(--fourthcolor);
    cursor: pointer;
}

.clicked {
    background-color: red;
}
.clicked:hover {
  background-color: red;
}

.firstletter {
    background-color: var(--maincolor);
    color: var(--fourthcolor);
    height: 20px;
    width: 20px;
    border-radius: 1px;
    text-align: center;
    margin-left: 5px;
}

.answer {
    color: var(--maincolor)
}

.datas {
    background-color: var(--secondcolor);
    margin: 20px 10px;
    padding: 20px;
    border-radius: 5px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

#name, #email {
    width: 80%;
    height: 40px;
    padding: 10px;
    border-radius: 6px;
    font-style: italic;
}

.submit {
    background-color: var(--fourthcolor);
    color: var(--maincolor);
    text-transform: uppercase;
    border-radius: 6px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    width: 200px;
    height: 50px;
    border: 2px solid var(--fourthcolor);
}
.submit:hover {
    background-color: var(--secondcolor);
    color: var(--fourthcolor);
    border: 2px solid var(--fourthcolor);
    cursor: pointer;
}

.results {
    margin: 20px 10px;
    padding: 20px;
    border-radius: 5px;
    background: linear-gradient(180deg, var(--secondcolor) 0%, var(--thirdcolor) 35%, var(--fourthcolor) 100%);
    text-align: justify;
}

.results h2 {
    text-align: center;
}

#alexandra {
  border-radius: 50%;
}

@media only screen and (min-width: 930px) {
    * {
      font-size: 20px;
    }

    .submit {
        padding: 50px;
    }
    .firstletter {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .introduction {
        margin: 50px 10px;
    }

    .questions {
        width: 900px;
        margin: auto;
    }

    .datas {
        width: 75%;
        margin: 100px auto;
    }
}
</style>
