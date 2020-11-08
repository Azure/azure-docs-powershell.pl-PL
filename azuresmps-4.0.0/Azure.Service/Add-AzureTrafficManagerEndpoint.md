---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055342"
---
# Add-AzureTrafficManagerEndpoint

## STRESZCZENIe
Dodaje punkt końcowy do profilu usługi Traffic Manager.

## POLECENIA

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureTrafficManagerEndpoint** umożliwia dodanie punktu końcowego do profilu usługi Microsoft Azure Traffic Manager.
Po dodaniu punktu końcowego przekazanie wyniku do polecenia cmdlet **Set-AzureTrafficManagerProfile** przy użyciu operatora potoku.
To polecenie cmdlet łączy się z usługą Azure, aby zapisać zmiany.

## Przykłady

### Przykład 1. Dodawanie punktu końcowego do profilu
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureTrafficManagerProfile** w celu uzyskania profilu o nazwie ContosoProfile, a następnie zapisanie go w zmiennej $TrafficManagerProfile.

Drugie polecenie dodaje punkt końcowy do profilu usługi Traffic Manager przechowywanego w $TrafficManagerProfile.
Punkt końcowy ma nazwę domeny Contoso02App.couldapp.net.
To polecenie określa również, czy jest włączone, oraz typ.
Polecenie przekazuje obiekt profilu do polecenia cmdlet **Set-AzureTrafficManagerProfile** , aby połączyć się z usługą Azure w celu zapisania zmian.

### Przykład 2: Dodawanie punktu końcowego z określoną lokalizacją i wagą
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

To polecenie umożliwia dodanie punktu końcowego do profilu usługi Traffic Manager.
Punkt końcowy ma nazwę domeny Contoso02App.couldapp.net.
To polecenie określa również, czy jest włączone, oraz typ.
Polecenie określa również wagę i lokalizację punktu końcowego.
Polecenie przekazuje obiekt profilu w celu **Ustawienia — AzureTrafficManagerProfile** , aby połączyć się z usługą Azure w celu zapisania zmian.

## PARAMETRÓW

### -NazwaDomeny
Określa nazwę domeny punktu końcowego, który ma zostać dodany.

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
Możliwe wartości to nazwy regionów platformy Azure, które wymieniono na liście https://azure.microsoft.com/regions/ .

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Określa obiekt profilu usługi Traffic Manager, do którego ma zostać dodany punkt końcowy.

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

Required: True
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

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


