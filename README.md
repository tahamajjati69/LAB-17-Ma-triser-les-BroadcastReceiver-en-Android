# LAB 17 : BroadcastReceiver Android

## Objectif
Application Android Java pour apprendre les BroadcastReceiver :
- Receiver dynamique : Mode Avion
- Receiver statique : BOOT_COMPLETED
- Broadcast personnalisé
- Gestion Android récent avec exported=false

## Technologies
- Android Studio
- Java
- Android SDK API 24+
- BroadcastReceiver
- Intent / IntentFilter

## Fonctionnalités
- Détecter activation/désactivation du mode avion
- Recevoir un événement au démarrage du téléphone
- Envoyer et recevoir un broadcast personnalisé
- Afficher les résultats avec Toast

## Structure
ReceiverDemo
├── MainActivity.java
├── AirplaneModeReceiver.java
├── BootReceiver.java
├── CustomEventReceiver.java
└── activity_main.xml

## Permission Manifest
<uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED"/>

## Receiver BOOT_COMPLETED
<receiver
    android:name=".BootReceiver"
    android:exported="false">
    <intent-filter>
        <action android:name="android.intent.action.BOOT_COMPLETED"/>
    </intent-filter>
</receiver>

## Résultat attendu
Au lancement :
Receiver Mode Avion : DÉSACTIVÉ

Après clic sur Activer :
Receiver Mode Avion : ACTIVÉ

Mode avion activé :
Mode Avion ACTIVÉ

Mode avion désactivé :
Mode Avion DÉSACTIVÉ

Custom Broadcast :
Custom Broadcast envoyé !
Custom reçu : Bonjour depuis le custom broadcast !

## Conclusion
Ce LAB montre la différence entre receiver dynamique et receiver statique, l’utilisation de onReceive(), IntentFilter, sendBroadcast(), registerReceiver() et unregisterReceiver(). <br>
<img width="372" height="833" alt="image" src="https://github.com/user-attachments/assets/85748518-4532-4e52-978f-eece3c6b2139" />
<img width="372" height="833" alt="image" src="https://github.com/user-attachments/assets/840d29c8-764a-4756-9005-58793f2af1a9" />

