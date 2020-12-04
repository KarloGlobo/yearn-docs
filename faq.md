---
title: faq.yearn.finance
tags: "docs, faq, published"
---

# Häufig gestellte Fragen

## FAQ - Frequenty Asked Questions

### Ist es sicher in Yearn zu investieren?

- Bitte unternimm deine eigenen Nachforschungen und entscheide dann für dich selbst.

### Gibt es ein audit? Wurde die Funktionalität der Yearn Finance Smart Contracts von unabhängigen dritten Überprüft?

- Ja, eine Liste der Audits findet sich [hier](https://github.com/iearn-finance/audits).

## Fragen & Lösungen

Bei Fragen aller Art findest du Hilfe unter:

- [Discord](http://discord.yearn.finance)
- [Telegram](https://t.me/yearnfinance)

Wenn du denkst es könnte etwas verbessert werden oder du einen Bug gefunden hast, wollen wir davon Wissen. Bitte teile deine Infos dazu hier:

- [Github](https://github.com/iearn-finance) — schildere die Begebenheiten in der jeweiligen Repository.
- [Forum](https://gov.yearn.finance/c/general-chat/feedback/2) — schreibe in die Feedback Kategorie.

## Produkte

### yearn.finance

- [yearn.finance](https://yearn.finance/) beherbergt die Seite für die Verwaltung von **Vaults**, **Earn**, **Zap**, **APR**, und **Cover** Produkten.

### Vaults

- [yearn.finance/vaults](https://yearn.finance/vaults)


#### Was ist ein Vault?

- In Vaults(engl. Tresore) werden Strategien zur Automatisierung der besten wirtschaftlichen Ertragsmöglichkeiten eingesetzt.
- Sie wurden so konzipiert, dass die Gemeinschaft gemeinsam neue Strategien entwickeln kann, um den besten Ertrag zu erzielen.
- Andre erklärt [Vaults](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613) und [delegierte Vaults](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2) in diesen beiden Blog-Beiträgen.
- Einfach ausgedrückt: Vaults können folgendes tun:
  - Jeden Vermögenswert als Liquidität nutzen.
  - Liquidität als Sicherheit verwenden und Sicherheiten auf einem sicheren Niveau verwalten, um einen Ausfall zu vermeiden.
  - Leihen Sie Stablecoins.
  - Setzen Sie die Stablecoins ein, um weitere ertragsmöglichkeiten zu generieren.
  - Nutzen Sie verdiente Stablecoins zum reinvestieren.

#### Kann ich das alles nicht einfach selbst machen?

- Ja, das könnten Sie, aber Vaults helfen Ihnen dabei, Transaktionskosten zu sparen, ein gutes Verhältnis zwischen Sicherheiten und Schulden zu halten, um Ausfälle zu vermeiden, und automatische Optimierungen für die ertragreichsten Stablecoin-Strategien vorzunehmen, selbst wenn Sie schlafen.

#### Ich sehe ROI auf der Seite der Vaults. Ist es die aktuelle?

- Nein. Dies ist der historische Durchschnitt für diesen Vault. Die aktuellen APY/Renditen werden nicht angezeigt, da es sich bei den Tresoren um ein Beta-Produkt handelt, das live getestet wird.
- Verschiedene Websites von Drittanbietern bieten APY und andere Informationen an; sie sind unten unter [Statistik] (https://docs.yearn.finance/faq#statistics) aufgeführt.

#### Was sind die Risiken?

- Während die hinterlegten Vermögenswerte nicht abnehmen können, kann sich die Verschuldung des Vaults erhöhen. Wenn eine Strategie es nicht schafft, die Schulden zu übertreffen, wird ein Teil des Vermögens vorübergehend gesperrt. Wenn es einer Strategie später wieder gelingt, die Verschuldung zu übertreffen, steht das Vermögen wieder zur Auszahlung zur Verfügung. Es gibt Mechanismen in den Vaults die dies verhindern, aber nichts ist kugelsicher.
- Bis jetzt sind nur _einige_ Vaults [geprüft] worden (https://github.com/iearn-finance/yearn-audits/blob/bdb3868c98e4fe2427898db05154942a9192efb1/MixBytes%20-%20Yearn.Finance%20protocol%20v.1%20Smart%20Contracts%20Audit%20Security%20Audit%20Report.pdf).
- Grundsätzliche Smart-Contract und Protokoll Risiken bei allen Schnitstellen, mit denen die Vaults interagieren.

#### Was sind die verschiedenen yTresorräume?

**yLINK und yaLINK**

- **Was ist der Unterschied zwischen LINK und aLINK Vaults?**
  - Keiner in Bezug auf die Erträge. Eingezahlter LINK wird in Aave eingezahlt, der aLINK generiert \(Aave verzinslicher LINK\). Wenn Sie also direkt in den aLINK Tresor einlegen, sind Sie in diesem Prozess einen Schritt voraus.
- **Warum ist der Ertrag bei aLINK und LINK Vaults unterschiedlich?**
  - aLINK hat eine Versicherungs-"Gebühr" von 0,5% \(diese wird zurückgezahlt, wenn sie übertroffen wird\). Der LINK Tresor hat diese Gebühr nicht, um doppelte  Gebühren zu vermeiden.

**yETH and yWETH**

- **Was ist der Unterschied zwischen WETH und ETH-Vaults?**
  - Keiner in Bezug auf die Rendite. ETH wird bei der Einlage in den Vault sowieso in WETH umgewandelt(wrapped). Der WETH-Tresor macht es für andere Ethereum-Protokolle nur einfacher, mit diesem Vault zu interagieren.
- **Wie schützt sich der ETH-Vault vor der Liquidation?**
  - Dieser Vault liest den ETH-Preis direkt aus dem Maker OSM \(Oracle Security Model\), einem System, das den Oracle-Preis 1 Stunde im Voraus liest. Dies gibt dem Tresor 1 Stunde Zeit, um die Collaterized-Debt-Position(CDP) Schulden vor der Liquidation zu bezahlen. Außerdem erhöht der Tresor die Besicherung weiter, indem er bei jedem Harvest-Call einen Gewinn hinterlegt.

**Andere Vaults**

- v1 Vaults, früher iEarn genannt, finden Sie [hier](https://yearn.finance/earn).
- Weitere Vaults finden Sie [hier](https://yearn.finance/vaults).

#### Wenn die aktuelle Strategie für den yCRV-Vault das Farmen von CRV ist, wird es dann einfach zu meinem Kontostand hinzugefügt, wenn ich mich auszahlen lasse?

- Nein. Der Vault wird CRV farmen und es dann automatisch auf dem Markt verkaufen. Wenn Sie sich auszahlen lassen, erhalten Sie mehr yCRV.

#### Warum ist yCRV nicht \$1 wert, es ist doch eine Stablecoin, oder?

- Nein, yCRV ist nicht \$1 wert, und nein, es ist KEIN Stablecoin. Sie können sich den yCRV als einen Index von renditetragenden Stablecoins \(yDAI+yUSDC+yUSDT+yTUSD\\) vorstellen, der ebenfalls Rendite generiert \(Handelsgebühren aus dem Curve Y Pool\). Daher ist der Preis von yCRV nicht fallend.

#### Wenn ich mein yCRV aus dem yCRV-Vault entnehme, wird es dann wieder in den Curve Y-Pool bei Curve zurückgeführt, oder muss ich etwas anderes tun, um es dort zurückführen?

- Wenn Sie Ihr yCRV aus dem Vault entnehmen, erhalten Sie yCRV + (aufgelaufene Zinsen - Gebühren) zurück, alles in yCRV. Da es sich um den yCRV-Token handelt, den Sie zurückbekommen haben, ist er bereits im Curve Y-Pool eingesetzt, was zu Stablecoin-Swap-Gebühren führt. Sie brauchen mit Curve nichts weiter zu tun, es sei denn, Sie wollen es [hier] (https://dao.curve.fi/minter/gauges) einsetzen, um CRV zu erzeugen.

#### Warum können wir keinen besseren APY für den YFI-Tresor bekommen?

- Man kann nicht die gleichen Erträge für zwei völlig unterschiedliche Coins bekommen. Der neue sBTC verfolgt die gleiche Strategie wie der YCRV Vault mit Curve Liquidity Pool. Die offensichtliche Antwort ist, dass es nicht viele sichere Plattformen gibt, die YFI als Sicherheit akzeptieren, so dass es im Moment nicht viele ertragreiche Strategien für den YFI-Vault gibt.

#### Ich habe in einen Vault eingezahlt, was bekomme ich zurück, wenn ich mich aus dem Vault auszahlen lasse?

- Sie können nur den Krypto-Asset-Typ entnehmen, den Sie eingelegt haben.
- Sie erhalten den Betrag, den Sie ursprünglich eingezahlt haben, plus die Rendite die Sie verdient haben, abzüglich der Gebühren.

#### Wie hoch sind die Gebühren?

- **0,5% Gebühr** auf Gelder, die von aktiven Strategien ausgezahlt werden
  - In jedem Vault ist ein gewisser Anteil des Gesamtfonds ungenutzt und die meisten von ihnen sind in der Strategie aktiv. Die ungenutzten Mittel sind die Differenz zwischen den "Vaultbeständen" und den "Strategiebeständen". Sie können sie auf [feel the Yearn](https://feel-the-Yearn.app/) sehen.
  - Wenn Sie Ihre Gelder aus den ungenutzten Mitteln abheben, werden Ihnen keine Abhebungsgebühren berechnet. Wenn sie aus den Strategiebeständen stammen, wird Ihnen die 0,5%ige Gebühr berechnet.
- **5% Gebühr** auf zusätzliche Rendite
  - Für gemeinschaftlich entwickelte Strategien, wie den neuen YETH-Tresor, gehen derzeit 10% dieser Gebühr an den Ersteller der Strategie. Die restlichen 90% gehen an die Schatzkammer und werden dann an die Governance verteilt.

#### Können Sie die 5% Gebühr für den zusätzlichen Ertrag erklären?

- Früher wurde dies als "5% Gebühr auf subventioniertes Gas" bezeichnet, was buchstäblich jeden außer Andre verwirrte. Technisch gesehen handelt es sich nicht um eine Erfolgsgebühr - es ist eine Gebühr auf einige gewinnbringende Transaktionen, die hohe Transaktionskosten verursachen und für das interne Funktionieren des Vaults entscheidend sind.
- Jeder Vault hat mehrere Ebenen. Hier sind zwei Beispiele, die zeigen, wie diese Gebühr zustande kommt, wenn die Funktion `harvest()` aufgerufen wird.
- yCRV Vault Beispiel:
  - Level 1: Stablecoins werden auf den Geldmärkten verzinst \(compound, aave, dydx\)
  - Level 2: Die Token der Ebene 1 (yDAI, yUSDC, yUSDT und yTUSD\) werden dem yCRV-Pool als liquide Mittel zur Verfügung gestellt, um Handelsgebühren zu verdienen.
  - Level 3: Die Strategie verdient CRV-Token-Belohnungen, die sie in yCRV-** recycelt. Dies ist die einzige Stufe, auf der die 5% Gebühr genommen wird.**
- USDC Tresor Beispiel:
  - Level 1: Zinsen generieren für das Verleihen in Compound
  - Level 2: COMP an USDC liquidiert
  - Level 3: Die Strategie verdient DF-Token-Belohnungen von DForce, die geerntet und für USDC-** verkauft werden. Dies ist die einzige Stufe, auf der die 5% Gebühr genommen wird.**

#### Wozu werden die Gebühren genutzt?

- Sie gehen an einen speziellen Treasury [Smart-Contract] (https://etherscan.io/address/0x93A62dA5a14C80f265DAbC077fCEE437B1a0Efde).
- In der Schatzkammer bleiben sie bis zu einem Limit von \$500k, über diesen Betrag hinaus werden sie an den Governance Staking [Vertrag] weitergeleitet (https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992).

#### Wurden die Gebühren immer so genutzt?

- Nein, als Yearn begann, gingen sie direkt an die [Adresse] von Andre (https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c).
- Dann übergaben wir sie an die [Multisig](https://etherscan.io/address/0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52), und die Gebühren gingen direkt dorthin.
- Und vor unserer derzeitigen Governance v2 wurden die Einsatzprämien [hier](https://etherscan.io/address/0xb01419E74D8a2abb1bbAD82925b19c36C191A701) verteilt.

#### Ertrag

- Wir planen, in Zukunft ein Dashboard zu erstellen, das Ihren aktuellen APY von allen offenen Positionen die Sie haben übersichtlich darstellt. Derzeit zeigen wir das APY für die Vaults, da sie sich noch in der Beta-Phase befinden, nicht live aber es werden die aktuellen APY's etwa einmal täglich auf [twitter] (https://twitter.com/iearnfinance) gepostet. Sie können den Ertrag, den Sie erzielen grob schätzen, indem Sie sich die [aktuelle Strategie] (https://feel-the-Yearn.vercel.app/) ansehen und prüfen wie hoch der APY ist.
- Wenn z.B. der YCRV-Vault das CRV-Token farmt, können Sie den Ertrag auf [Curve's homepage](https://www.curve.fi/) für den Y-Pool überprüfen.

### Vault-Strategien

#### Was ist eine Vaultstrategie?

- Yearn's Vaultstrategien sind modulare, intelligente Smart-Contracts für jeden Tresor, in denen festgelegt ist welche Vermögenswerte ausgeliehen werden sollen, welche Vermögenswerte bewirtschaftet werden sollen und wo die bewirtschafteten Vermögenswerte verkauft werden sollen.

#### Was sind die aktuellen Strategien?

- Sie können die derzeit implementierten Strategien unter [feel-the-Yearn](https://feel-the-Yearn.vercel.app/) einsehen.
- Für die Zukunft planen wir die Erstellung eines Dashboards, um die Strategien und den APY leicht verständlich zu machen.

#### Wer hat die Kontrolle über die Strategien?

- Die Entwickler schreiben sie, aber die Multi-Sig, die von den YFI-Wählern angewiesen wird, entscheidet, ob sie umgesetzt werden oder nicht.

#### Wie kann ich eine Strategie entwickeln?

- Vorerst können Sie Ihre Strategie auf dem Forum in der Rubrik Strategie veröffentlichen. Geben Sie im Detail an, was sie kaufen/verkaufen/farmen soll und was der aktuelle APY ist. Es wird eine Vorlage geben, um Ihnen den Einstieg zu erleichtern.

#### Was ist der Prozess, um meine Strategie auf Yearn zu bringen?

- Veröffentlichen Sie sie im Forum oder nehmen Sie Kontakt mit dem Entwicklerteam auf. Wenn Sie Zustimmung für Ihre Idee erhalten und sie schließlich umgesetzt und genehmigt wird, wird sie in den Vaults verwendet und Sie können dafür bezahlt werden.

#### Wann ändert sich eine Strategie und wer ändert sie? Erfolgt sie automatisch?

- Strategieentwickler beobachten die Märkte und schreiben Strategien, die sie für sicher halten und gleichzeitig den höchsten Ertrag bringen. Sie ändern sie entsprechend den aktuellen Renditen auf dem Markt.

### Earn

- [yearn.finance/earn](https://yearn.finance/earn)

#### Was ist Earn?

- Earn ist ein Ertragsaggregator für Kreditplattformen, der während der Vertragsinteraktion für höchste Erträge sorgt.
- Hinterlegen Sie DAI, USDC, USDT, TUSD oder sUSD und es wird automatisch zum höchsten Kreditzinssatz auf diesen Plattformen [Compound](https://compound.finance/), [Dydx](https://dydx.exchange/) oder [Aave](https://app.aave.com/home) \(Ddex und Fulcrum sind derzeit deaktiviert\) ausgeliehen.
- Erfahren Sie mehr in den [Yearn Docs](https://docs.yearn.finance/products/earn)

### Zap

- [yearn.finance/zap](https://yearn.finance/zap)

#### Was ist Zap?

- Mit Zap können Benutzer unterstützte Tokens mit nur einer Vertragsinteraktion umwandeln, um Transaktionskosten zu reduzieren.
- Zaps wurden von DefiZap hergestellt, das jetzt [Zapper.fi] (https://zapper.fi) als eine Art All-in-one DeFi-Routing-Dienst ist.

#### Warum einen Zap verwenden?

- "Zaps ermöglichen es Ihnen, in einer Transaktion in eine DeFi-Position zu gelangen - das nennt man Zapping in". - Anleitung zur Verwendung von Zaps](https://defitutorials.substack.com/p/how-to-use-defizap).
  - Beachten Sie, dass es sich hierbei um einen alten Artikel handelt und [Zapper](https://zapper.fi) entstand als Ergebnis der Zusammenführung von DeFiSnap + DeFiZap, um den ultimativen Knotenpunkt für Dezentralisierte Finanzen alias \#DeFi zu schaffen. Daher ist einiges von dem Zeug in dem obigen Artikel veraltet, aber Sie können Zaps immer noch auf Zapper.fi verwenden.

#### Was kann ich also mit Zaps auf Yearn tun?

- Mit einem Zap können Sie z.B. Ihren DAI nehmen und mit ihm yCRV in einer Transaktion erhalten. Normalerweise müssten Sie, um DAI in yCRV zu verwandeln, zu Earn gehen, DAI einzahlen und yDAI erhalten, dann auf [Curve.fi - Yearn pool](https://www.curve.fi/iearn/deposit) gehen und Ihren yDAI einzahlen und dann yCRV erhalten. Das ist eine Menge zu tun, stattdessen können Sie es in einer Transaktion erledigen!

#### Das klingt fantastisch, was ist der Nachteil?

- Nun, es erfordert eine Menge Gas und könnte kostspieliger sein, sogar noch teurer als es selbst manuell zu tun, aber wenn Sie eine große Transaktion haben und in Eile sind, ist es eine großartige Methode, um schnell in eine DeFi-Position oder einen Liquiditätspool zu kommen.

### yInsure / Cover

- [yinsure.finance] (https://yinsure.finance/)

#### Was ist yInsure?

- yInsure, auch bekannt als **Cover**, ist ein gepooltes Deckungssystem, das eine Versicherung gegen intelligente Vertragsrisiken bietet.
- Es hat keine KYC-Anforderung und wird von Nexus Mutual bereitgestellt.
- Erfahren Sie mehr in diesem [Artikel](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896).

### Produkte derzeit in Forschung und Entwicklung

#### yTrade

- [ytrade.finance](https://ytrade.finance/)
- Leveraged Stable Coin Trades \(testnet\).

#### yLiquidate

- [yliquidate.finance] (https://yliquidate.finance/)
- 0 Kapital automatisierte Liquidationen für Aave \(testnet\).

#### ySwap

- [yswap.exchange] (https://yswap.exchange/)
- Einseitig automatisierter Market Maker \(Test im Mainnet\).

#### yBorrow

- [yborrow.finance] (https://yborrow.finance/)
- Kreditdelegation Vaults von Smart-Contracts zu Smart-Contracts für die Kreditvergabe\(testnet\).

## Kommunikation

- [Forum](https://gov.yearn.finance)
  - Über das Telegramm und Discord wird viel in Echtzeit diskutiert, aber damit aus einem Vorschlag ein YIP \(Yearn Improvement Proposal\) wird, muss er im Forum gepostet und diskutiert werden.
  - Dies ist der wichtigste Ort, an dem Token-Inhaber nach Governance-bezogenen Fragen suchen.
- [Discord](http://discord.yearn.finance/)
  - Einschließlich nicht-englischer Kanäle.
- [Telegramm](https://t.me/yearnfinance) - Hauptchat.
- [Telegramm](https://t.me/yearncommunity) - Chat Handel/Soziales/Support.
- Twitter
  - [yearn.finance] (https://twitter.com/iearnfinance?s=20) - Offizieller Twitter von Yearn
  - [Andre Cronje](https://twitter.com/AndreCronjeTech?s=20) - Gründer und Schöpfer von Yearn
  - [yLearnfinance](https://twitter.com/yLearnfinance) - Yearn Info
  - [learn2yearn](https://twitter.com/learn2Yearn) - Yearn Info

## Governance

### Alles über YIPs

#### Was ist ein YIP? Warum sind sie wichtig?

- Ein YIP oder Yearn Improvement Proposal ist die Art und Weise wie Funktionen zum Yearn Ökosystem hinzugefügt werden. BenutzerInnen starten einen Vorschlag im Forum, diskutieren ihn und beurteilen, ob der Vorschlag angenommen wird. Wenn viele Benutzer mit dem Vorschlag einverstanden sind wird er on-Chain veröffentlicht werden, damit alle darüber abstimmen können.

#### Wie viele Personen müssen abstimmen, um ein auf der Kette vorgeschlagenes YIP zu verabschieden?

- Das Quorum beträgt 20%. Das bedeutet, dass 20% der staked YFI über einen Vorschlag abstimmen müssen, damit er angenommen wird andernfalls wird er scheitern. Ausserdem müssen mindestens 50% der Stimmen für Ja stimmen.
- Sie können Ihren Vorschlag zuerst selbst on-Chain veröffentlichen, aber wenn die Leute noch nicht darüber gesprochen haben werden sie wahrscheinlich nicht dafür stimmen.

#### Wie mache ich einen Vorschlag?

- Die Standardvorlage für Vorschläge finden Sie unter [Github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md) + im [Forum](https://gov.yearn.finance). Wenn Sie unter Vorschläge oder Diskussion einen Beitrag verfassen, füllt sich die Vorlage automatisch.
- Das Verfahren ist ungefähr:
  1. Diskussion im Forum
  2. zum YIP befördern \ (normalerweise durch Mods\), YIP zum Github hinzufügen, on-Chain setzen
  3. ankündigen

#### Wer kann einen Vorschlag machen?

- Jeder kann einen Vorschlag sowohl im Forum als auch on-Chain veröffentlichen.

### Abstimmen

#### Wie stimme ich ab?

- Staken Sie Ihr YFI, damit können Sie Ihre Stimme für YIPs abgeben, die auf dem Voting [Dashboard] (https://ygov.finance/vote) on-Chain sind.

#### Kann ich abstimmen, wenn sich mein YFI im YFI-Vault befindet?

- Nein, Ihre YFI muss in den Governance [Vertrag] (https://ygov.finance/staking) staked sein, um abstimmen zu können.

#### Wo kann ich die YIPs einsehen?

- Sie können sie auf dem Voting [Dashboard](https://ygov.finance/vote) einsehen, wenn Sie sich in Ihr web3-Konto einloggen oder unter [yips.yearn.finance](https://yips.yearn.finance/all-yip).

#### Warum sollte ich mich beteiligen? Was ist der APY \(Annual Percentage Yield\)?

- Sie sollten einen Einsatz leisten, wenn Sie über YIPs abstimmen und Belohnungen erhalten möchten die aus dem Yearn Ökosystem generiert werden. Der APY für das Abstimmen ist derzeit nicht auf der UI aufgeführt. Sie können im Chat fragen, wie hoch der Satz ist.

#### Was muss ich tun, um Belohnungen mit meinem YFI zu erhalten?

- Alles, was Sie tun müssen, ist YFI bei [ygov.finance/stake] (https://ygov.finance/stake) zu staken, und Sie erhalten eine Belohnung wenn die Treasury bei oder über $500k liegt. Sie können die Adresse der Treasury [hier] überprüfen (https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52).
- Beachten Sie, dass Sie bei einem Staking Belohnungen erhalten (solange diese nicht an die Treasury gehen), aber Sie können sie nur innerhalb von 3 Tagen nach der Abstimmung einfordern.

#### Ist es für die Abstimmung von Bedeutung, mein YFI zu Staken?

- Ja. Sie müssen Ihr YFI unter [ygov.finance/stake] (https://ygov.finance/stake) in der Registerkarte v2 unter Governance V2 staken damit Ihre Stimmen zählen. Ab sofort können Sie ohne Staking abstimmen, aber Sie verschwenden Ihr Gas und es wird nicht gezählt, also stellen Sie sicher dass Sie zuerst YFI gestaked haben, wenn Sie abstimmen wollen.

#### Was ist, wenn ich mein YFI vor dem Ende der Abstimmungssperre herausnehmen möchte?

- Das können Sie nicht, technisch nicht möglich. Die Sperre dauert 3 Tage, nachdem Sie das letzte Mal gewählt haben, bis dahin können Sie Ihre Token nicht mehr herausnehmen.
- Wenn Sie versuchen, Ihre Token vor dem Ende der Sperre zu unstaken, werden Sie sehr hohe Transaktionskosten haben. Dies ist ein Fehler, Sie können Ihre Token erst unstaken, wenn die dreitägige Sperre abgelaufen ist.

#### Ich habe gewählt und weiß, dass die Sperrfrist für die Abstimmung 3 Tage beträgt. Kann ich irgendwo genau sehen, wie lange mir noch bleibt, bis ich mein YFI aufheben kann?

- Ja! Sie können den Vertrag direkt lesen [ygov.finance-Staking-Vertrag](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract) Gehen Sie zu 28 votelock und geben Sie Ihre Ethereum Adresse ein. Dadurch erhalten Sie die Nummer des eth-Blocks, an dem Sie sich abstimmen können.

#### Was ist der Unterschied zwischen einer Abstimmung im Forum und einer Abstimmung on-Chain?

- Eine Umfrage misst nur die Meinung der Gemeinschaft über den Vorschlag, während eine Abstimmung on-Chain bindend ist und wirksam wird, wenn sie angenommen wird.

#### Was ist mit der neuen Sache bezüglich Abstimmen ohne Transaktionskosten?

- Wir haben jetzt ein Off-Chain-Signalsystem, das mit staked Balances von Ygov arbeitet. Dies ersetzt die älteren informellen Forumsabstimmungen, die anfällig für Sybil-Angriffe waren. Es kann Multiple-Choice-Abstimmungen durchführen und kostet keine Transaktionskosten, Sie unterschreiben stattdessen mit Ihrer Wallet. Wir benutzen immer noch das normale On-Chain-Abstimmungssystem für YIPs.

#### Wie lange ist mein YFI gesperrt, wenn ich es stake?

- Ihr YFI ist für 3 Tage nach Ihrer Wahl gesperrt.

#### Warum kann ich meine Einsatzprämien nicht beanspruchen?

- Um Ihre Einsatzprämie zu beanspruchen, müssen Sie 1\) staked sein und 2\) innerhalb von 3 Tagen abgestimmt haben, um sie beanspruchen zu können. Dies wird demnächst in einem Update behoben werden.

### yDAO

- Pokemol [site](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862/).
- Forum [Beitrag](https://gov.yearn.finance/t/ydao-for-community-funding/2243).

#### Was ist der Zweck von yDao?

- Es dient zur Finanzierung von Beiträgen mit Mehrwert für das Ökosystem von Yearn.

#### Wen interessiert das, wie kann ich damit Geld verdienen?

- Es interessiert Sie nicht. Es dient ausschließlich der Zuweisung von Mitteln für Projekte und die gespendeten YFI werden ausgegeben, Ihr Anteilswert wird verwässert.

#### Wer kann beitreten?

- Jeder kann beitreten mit einem Basiszinssatz von 1 Anteil = 0,1 YFI.

#### Wie kann ich beitreten?

- Gehen Sie  zu [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) und melden Sie sich mit Ihrem web3-Konto an. Klicken Sie oben rechts auf die Schaltfläche Neuer Vorschlag. Klicken Sie auf Mitglied.
  - Title: Ihr Name/Ihre Entität
  - Description: "Verpfändung eines Betrages X in YFI im Tausch gegen Y-Shares" \(Bitte stimmen Sie dies mit dem Betrag ab, der mit 0,1 YFI pro Aktie verpfändet wird\)
  - Link: Link zu Ihnen oder Ihrer Entität \(Website, Twitter, Linkedin\)
  - Shares Requested: Die Anzahl der beantragten Shares
  - Token Tribute: Der Betrag des YFI, der verpfändet wird \ (Sie müssen YFI freischalten\)
  - Loot: Die Anzahl der angeforderten Shares
  - Nachdem Sie die beiden Transaktionen eingereicht haben und sich in der Warteschlange für neue Mitglieder befinden benötigen Sie einen Sponsor. Bitte kopieren Sie den Link zu Ihrem Vorschlag und teilen Sie uns mit, dass Sie am [yDAO Telegrammkanal] (https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA) teilnehmen möchten.

#### Wie kann ich eine Finanzierung beantragen?

- Auf die gleiche Weise wie beim Beitritt, außer dass Sie statt auf "Mitglied" auf die Registerkarte "Finanzierung" klicken und die Details Ihres Antrags ausfüllen. Sie können im [Telegramm-Chat] (https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA) fragen, wenn Sie Fragen haben.

#### Ich spreche kein Englisch, wann wird alles übersetzt?

- Wir arbeiten daran in andere Sprachen zu übersetzen, aber das wird Zeit brauchen. Vorerst können Sie Ihre Sprache in der globalen Sektion in [Discord](http://discord.yearn.finance/) wählen.

## Gemeinschaft

### Hat Yearn ein Manifest?

- Einige Beitragende haben sich zusammengetan und einen Beitrag darüber geschrieben, wie sie über das Protokoll denken, und andere haben mitgemacht, um es zu unterstützen. Es ist [im Forum] verfügbar (https://gov.yearn.finance/t/how-we-think-about-yearn/).

### Ist Andre Cronje für Yearn verantwortlich?

- Andre ist nicht für Yearn zuständig, die YFI-Token-Inhaber treffen die Entscheidungen darüber, wie Yearn zu verwalten ist, Andre ist einer der Entwickler im Yearn-Ökosystem.

### Was ist die Multisig und was tun sie?

- Die Ausführung von Transaktionen mit mehreren Signaturen wird in diesem [Thread](https://gov.yearn.finance/t/yfi-minting-ownership/155) ausführlich erläutert. Im Grunde handelt es sich um ein Konto mit 6 von 9 Mehrfachsignaturen, das die Kontrolle über die Vergabe von YFI hat, wenn eine Abstimmung zur Prägung von Wertmarken erfolgreich abgeschlossen wurde.

### Wer sind die 9 Multisignier-Unterzeichner?

- [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
- [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
- [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
- [Banteg](https://twitter.com/bantg/status/1285426492906909696)
- [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)
- [Joe Mahon aka Substreight](https://twitter.com/Substreight/status/1299780260737630209)
- [Tarun Chitra, Fehdehandschuh](https://twitter.com/gauntletnetwork/status/1299778153674616833)
- [Wasilij Schapowalow, p2p.org](https://twitter.com/_vshapovalov/status/1299799139635679232)
- [Mariano Conti, ehemaliger HerstellerDAO](https://twitter.com/nanexcool)

### Haben sich die Multisig-Signatoren geändert?

- Ja, [YIP-40](https://gov.yearn.finance/t/yip-40-replace-inactive-multisig-signers/3535) hat vier der Unterzeichner gewechselt.
- Ausgehende Unterzeichner waren:
  - [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
  - [Michael, Kurve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
  - [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976)
  - [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073)

### Welche Entscheidungen kann Andre allein treffen?

- Andre kann das Yearn-Ökosystem aufbauen und neue Produkte entwickeln. Gewöhnlich veröffentlicht er seine Gedanken und Ideen im [Forum](https://gov.yearn.finance) oder in seinem [Medium-Blog](https://andrecronje.medium.com) so dass jeder sie sehen kann.

### Sagt ihm die Multisig-Gruppe, was er tun soll?

- Sie stehen in engem Kontakt miteinander, aber die Prioritäten von Andre sind seine eigenen. Sie können über YIPs instruiert werden.

### Wer schreibt sonst noch Code für Yearn? Gibt es ein Team?

- Gibt es ein Team? Ja! Lernen Sie einige der Entwickler hinter Yearn kennen:

  - [@banteg](https://gov.yearn.finance/u/banteg)
  - [@fubuloubu](https://gov.yearn.finance/u/fubuloubu)
  - [@x48](https://gov.yearn.finance/u/x48)
  - [@doug](https://gov.yearn.finance/u/doug)
  - [@luciano](https://gov.yearn.finance/u/luciano)
  - [@orbxball](https://gov.yearn.finance/u/orbxball)

### Wird jemand für die Arbeit an Yearn bezahlt?

- Ja. Yearn hat ein Kernteam, das wiederkehrende Zahlungen erhält. Außerdem werden monatlich Zuschüsse an helfende Mitarbeiter verteilt. Siehe zum Beispiel die [September Grants Announcement](https://gov.yearn.finance/t/september-grants-announcement/7044).

### Wie kann ich für Yearn arbeiten?

- Wenn auch Sie zum Projekt beitragen möchten, wenden Sie sich einfach an unsere Community-Manager unter [Discord](http://discord.yearn.finance/)/[Telegramm](https://t.me/yearnfinance)/[Twitter](https://twitter.com/iearnfinance). Demnächst werden wir auch einen Leitfaden für Contributoren veröffentlichen.

Übersetzt mit www.DeepL.com/Translator (kostenlose Version)

### Haben Sie Stellenangebote?

- Ja, die haben wir! Wir brauchen alle möglichen Leute, die dazu beitragen, das Yearn Ökosystem zu einem blühenden Produkt zu machen und YFI einen Wert zu verleihen. Sie können in Discord oder Telegramm nach einer Bewerbung fragen. Geben Sie an wie Sie glauben, dass Sie Yearn einen Mehrwert verleihen können und wie viel Sie Ihrer Meinung nach aus dem Gemeinschaftspool bezahlt werden sollten. Sie können sich auch an die [yDAO] (https://gov.yearn.finance/t/ydao-for-community-funding/2243) wenden um Mittel für Ihre Arbeit für das Ökosystem von Yearn zu erhalten.

### Wie kann man sich beteiligen?

- Sie können sich an YFI beteiligen, indem Sie über YIPs abstimmen die aktiv sind, die noch vorzuschlagenden YIPs on-chain in den Foren diskutieren und über YFI im Telegram und Discord sprechen. Wenn Sie eine zweite Sprache beherschen, helfen Sie uns die Website und die YIPs in diese Sprache zu übersetzen.

### Laufende Bemühungen zur Verbesserung des Yearn Ökosystems

- Sie können die aktiven YIPs [hier] ansehen (https://yips.yearn.finance/all-yip)

## Benutzerschnittstelle

### Kann ich die Yearn ecosystem dApps auf meinem Telefon verwenden?

- Ja, Sie müssen den Metamask-Browser verwenden.

## Technische Unterstützung

### Ich habe meine ETH-Transaktion abgeschickt, aber da steht ausstehend? Wie kann ich das beheben?

- Sie sollten immer darauf achten dass Sie Ihre Transaktionskosten(Gas) richtig einstellen, wenn Sie wollen dass eine Transaktion schnell durchgeführt wird. Prüfen Sie die aktuellen Gaspreise unter [Ethgasstation] (https://ethgasstation.info/) oder [gasnow] (https://www.gasnow.org/).
- Wenn Sie die MetaMask verwenden und Ihre Transaktion durchlaufen lassen, sie aber zu langsam läuft haben Sie die Möglichkeit sie zu beschleunigen, indem Sie unter "Aktivität" auf die Schaltfläche "Beschleunigen" unter Ihrer letzten ausstehenden Transaktion klicken. Dies sollte den gleichen TX noch einmal mit einem höheren Gaspreis senden, um ihn schneller bestätigt zu bekommen.
- Wenn Sie alles versucht haben und Ihre Transaktion immer noch in der Schwebe ist können Sie das Problem beheben indem Sie eine Transaktion an die Nonce der ersten "stuck" Transaktion mit einem hohen Gaspreis senden, um die "stuck" Warteschlange zu überschreiben. Hier ist ein guter [Leitfaden](https://ethgasstation.info/blog/stuck-transaction-guide) der erklärt, wie man das macht.

### Warum ist die Rücknahmegebühr so hoch?

- Wenn die Gebühren während der Nutzung des Yearn Ökosystems höher als normal sind, dann kann das an der Überlastung des Ethereum und den ungewöhnlich hohen Gaskosten liegen. Siehe [Ethgasstation] (https://ethgasstation.info/). Sie haben die Wahl: Warten Sie bis die Gaspreise fallen, oder geben Sie das Geld aus um Ihre Transaktion jetzt abzuwickeln.
- Wenn die Gaspreise wahnsinnig hoch sind, bedeutet dies dass ein Fehler vorliegt und die Transaktion nicht bearbeitet werden kann. Zum Beispiel, wenn Sie versuchen einen Token einzuzahlen den Sie nicht haben, oder wenn es keine Deckung für einen Vertrag unter [http://yinsure.finance/](http://yinsure.finance/) gibt.

## Verwandte Projekte


### [Curve](https://www.curve.fi)

- Curve ist ein Börsen-Liquiditätspool auf Ethereum \(wie [Uniswap] (https://app.uniswap.org/#/)\), der für \(1\) extrem effizienten Handel mit stabilen Münzen \(2\) risikoarmes, zusätzliches Gebühreneinkommen für Liquiditätsanbieter, ohne Opportunitätskosten, konzipiert wurde. Curve ermöglicht es Benutzern \(und intelligenten Kontrakten wie 1inch, Paraswap, Totle und Dex.ag\), zwischen dem DAI und der USDC mit einem maßgeschneiderten Algorithmus mit geringer Slippage und niedrigen Gebühren, der speziell für Stablecoins entwickelt wurde, zu handeln und Gebühren zu verdienen. Hinter den Kulissen wird der Liquiditätspool auch an das Compound-Protokoll oder yearn.finance geliefert, wo er noch mehr Einnahmen für die Liquiditätsanbieter generiert.
- Kurve [FAQ](https://www.curve.fi/rootfaq).

### [Aave](https://app.aave.com/home)

- Aave ist ein Open-Source-Protokoll ohne Freiheitsentzug, das die Schaffung von Geldmärkten ermöglicht. Die Benutzer können Einlagen verzinsen und Vermögenswerte ausleihen.

## Ressourcen

### Wo kann ich mehr über Yearn erfahren?

- [Yearn lernen](https://www.learnyearn.finance/)
- [Medium.com/erwerben](https://medium.com/iearn)
- [yCosystem](https://ycosystem.info/)

### Lists of Smart Contracts

- [https://gov.yearn.finance/t/yearn-contracts/1951](https://gov.yearn.finance/t/yearn-contracts/1951)
- [https://etherscan.io/accounts/label/yearn-finance](https://etherscan.io/accounts/label/yearn-finance)
  - sign-in required
- [Delegated controller](https://etherscan.io/address/0x2be5d998c95de70d9a38b3d78e49751f10f9e88b#readContract)
- [StrategyVaultTUSD](https://etherscan.io/address/0x35CEE4c61B7619956e0B2015B5411F93CBba817A#code)
- [yLINK token](https://etherscan.io/address/0x881b06da56bb5675c54e4ed311c21e54c5025298#code)
- [yaLINK token](https://etherscan.io/address/0x29e240cfd7946ba20895a7a02edb25c210f9f324#readContract)
- [StrategyMStableSavingsTUSD](https://etherscan.io/address/0xd6214317bf66921154d78e3074bada013a4de8e8#readContract)
- [yTUSD](https://etherscan.io/address/0x37d19d1c4e1fa9dc47bd1ea12f742a0887eda74a)
- [yTokenRebalance](https://etherscan.io/address/0x19b6424C58aFcee6D0cb954D4B8d44B9b5e9cC09#code)
- [CollateralVaultProxy](https://etherscan.io/address/0xf0988322b8392245d6232e520bf3cdf912b043c4)
- [USDC strategy for LINK](https://etherscan.io/address/0x25fAcA21dd2Ad7eDB3a027d543e617496820d8d6)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [DAI vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952)

### Registry of Tokens and Utility Contracts

- [https://docs.yearn.finance/developers/deployed-contracts-registry](https://docs.yearn.finance/developers/deployed-contracts-registry)

### Vaults Detail Reference

- [https://vaults.finance/](https://vaults.finance/)

### Statistics

- [yieldfarming.info](https://yieldfarming.info/)
- [yVault ROI Calculator](https://py-earn.herokuapp.com/)
- [stats.finance/yearn](https://stats.finance/yearn)
- [Feel The Yearn](https://feel-the-yearn.vercel.app/)
- Initial Distribution [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
- Voting Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)
- Vaults Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/g0bGfgloeXBd9C18jpBjdXi5KkQjR7IXYqFRUnHk)

### Latest Yearn News

- [yearn.finance](https://twitter.com/iearnfinance) - Offical Twitter of Yearn
- [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
- [Yearn Finance](https://medium.com/iearn) - Offical Blog

### Podcasts

- [Unchained - Andre Cronje on YFI and the Fair Launch: ‘I’m Lazy’](https://unchainedpodcast.com/andre-cronje-of-yearn-finance-on-yfi-and-the-fair-launch-im-lazy/)
- [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
- [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
- [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
- [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
- [YFI: Farming the Farmers \| Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

### Blogs

- [Yearn Finance - Offical Blog](https://medium.com/iearn)
  - [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
  - [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
  - [yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
  - [Yearn Governance Forum](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
  - [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
  - [YFI](https://medium.com/iearn/yfi-df84573db81)

### Logos

- Can be found in the Discord under [\#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)
