---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054400"
---
# Set-AzureTrafficManagerEndpoint

## STRESZCZENIe
Aktualizuje właściwości punktu końcowego w profilu usługi Traffic Manager.

## POLECENIA

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureTrafficManagerEndpoint** aktualizuje właściwości punktu końcowego w profilu programu Microsoft Azure Traffic Manager.
Jeśli punkt końcowy nie istnieje w bieżącym profilu, to polecenie cmdlet utworzy je.
Po dodaniu punktu końcowego przekazanie wyniku do polecenia cmdlet **Set-AzureTrafficManagerProfile** przy użyciu operatora potoku.
To polecenie cmdlet łączy się z usługą Azure, aby zapisać zmiany.

## Przykłady

### Przykład 1: aktualizowanie punktu końcowego dla profilu
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureTrafficManagerProfile** w celu uzyskania profilu o nazwie ContosoProfile, a następnie zapisanie go w zmiennej $TrafficManagerProfile.

Drugie polecenie aktualizuje punkt końcowy w profilu usługi Traffic Manager przechowywanych w $TrafficManagerProfile.
Punkt końcowy ma nazwę domeny ContosoApp02.cloudapp.net.
Polecenie określa również stan, typ, wagę i lokalizację punktu końcowego.
Polecenie przekazuje zmodyfikowany profil do polecenia cmdlet **Set-AzureTrafficManagerProfile** , aby połączyć się z usługą Azure w celu zapisania zmian.

## PARAMETRÓW

### -NazwaDomeny
Określa nazwę domeny punktu końcowego, który należy zmodyfikować.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację punktu końcowego, który jest dodawany przez polecenie cmdlet.
To musi być lokalizacja na platformie Azure.

Ten parametr musi zawierać wartość dla punktów końcowych typu "any" lub typu "Trafficmanager" w profilu, którego Metoda równoważenia obciążenia jest ustawiona na wartość "wydajność".
Możliwe wartości to nazwy regionów platformy Azure, które wymieniono na liście  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Określa minimalną liczbę punktów końcowych, które profil zagnieżdżony musi mieć w trybie online, aby ten punkt końcowy był traktowany jako dostępny.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Określa stan punktu końcowego monitorowania.
Prawidłowe wartości: 

- Wyłączona
- Łącza

Jeśli określisz wartość włączone, Usługa Traffic Manager monitoruje punkt końcowy, a metoda równoważenia obciążenia traktuje ją podczas zarządzania ruchem.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Określa obiekt profilu usługi Traffic Manager, dla którego ma zostać zmodyfikowany punkt końcowy.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Type
Określa typ punktu końcowego.
Prawidłowe wartości: 

- CloudService
- AzureWebsite
- Nr ruchu

- Jakieś 

Jeśli istnieje więcej niż jeden punkt końcowy AzureWebsite, punkty końcowe muszą znajdować się w różnych centrach danych.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waga
Określa wagę punktu końcowego, który jest dodawany przez polecenie cmdlet.
Prawidłowy zakres wartości dla tego parametru to \[ 1, 1000 \] .

Ten parametr jest wykorzystywany tylko w przypadku zasad równoważenia obciążenia RoundRobin.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition
To polecenie cmdlet generuje obiekt profilu usługi Traffic Manager, który zawiera informacje na temat zaktualizowanego profilu.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


