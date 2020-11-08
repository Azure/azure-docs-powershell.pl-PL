---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054760"
---
# Set-AzureTrafficManagerProfile

## STRESZCZENIe
Aktualizuje właściwości profilu usługi Traffic Manager.

## POLECENIA

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureTrafficManagerProfile** aktualizuje właściwości profilu Microsoft Azure Traffic Manager.

W przypadku profilów, dla których ustawiono wartość *LoadBalancingMethod* na "tryb failover", możesz określić kolejność przejęcia awaryjnego punktów końcowych dodanych do profilu za pomocą polecenia cmdlet Add-AzureTrafficManagerEndpoint.
Aby uzyskać więcej informacji, zobacz przykład 3 poniżej.

## Przykłady

### Przykład 1: Ustawianie wartości TTL dla profilu usługi Traffic Manager
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

To polecenie ustawia wartość TTL równą 60 sekund dla obiektu profilu usługi Traffic Manager MyTrafficManagerProfile.

### Przykład 2: Ustawianie kilku wartości dla profilu
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

To polecenie pobiera profil usługi Traffic Manager o nazwie Moja profil przy użyciu polecenia cmdlet **Get-AzureTrafficManagerProfile** .
W profilu jest używana metoda równoważenia obciążenia RoundRobin, czyli czas wygaśnięcia: 30 sekund, protokół monitorowania HTTP, port monitora i ścieżka względna profilu usługi Traffic Manager.

### Przykład 3: Zmienianie kolejności punktów końcowych na pożądaną kolejność w trybie failover
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

Ten przykład zmienia kolejność punktów końcowych dodanych do polecenia mój profil do wybranego zlecenia trybu failover.

Pierwsze polecenie pobiera obiekt profilu usługi Traffic Manager o nazwie Moja profil i zapisuje obiekt w zmiennej $Profile.

Drugie polecenie ponownie porządkuje punkty końcowe z tablicy punktów końcowych do kolejności, w której ma się odbywać przejście.

Ostatnie polecenie aktualizuje profil usługi Traffic Manager przechowywany w $Profile z nową kolejnością punktów końcowych.

## PARAMETRÓW

### -LoadBalancingMethod
Określa metodę równoważenia obciążenia używaną do rozpowszechniania połączenia.
Prawidłowe wartości: 

- Pracy
- Jęcie
- RoundRobin

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

### -MonitorPort
Określa port służący do monitorowania kondycji punktu końcowego.
Prawidłowe wartości to wartości całkowite większe niż 0 i mniejsze niż lub równe 65 535.

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

### -MonitorProtocol
Określa protokół, który ma być używany do monitorowania kondycji punktu końcowego.
Prawidłowe wartości: 

- URL
- Https

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

### -MonitorRelativePath
Określa ścieżkę względem nazwy domeny punktu końcowego do sondowania stanu kondycji.
Ścieżka musi być zgodna z następującymi ograniczeniami: 

- Ścieżka musi zawierać od 1 do 1000 znaków.
- Musi zaczynać się ukośnikiem/.
- Nie może zawierać żadnych elementów XML \<\> .
- Nie może zawierać podwójnych ukośników,//.
- Nie może zawierać nieprawidłowych znaków escape HTML.
Na przykład% XY.

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

### -Name (nazwa)
Określa nazwę profilu usługi Traffic Manager do zaktualizowania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -TrafficManagerProfile
Określa obiekt profilu usługi Traffic Manager używany do ustawiania profilu.

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

### -TTL
Określa czas wygaśnięcia (TTL) DNS, który informuje lokalnych nazw DNS, jak długo są buforowane wpisy DNS.
Prawidłowe wartości to liczby całkowite z zakresu od 30 do 999 999.

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
To polecenie cmdlet generuje obiekt profilu programu Traffic Manager.

## INFORMACYJN

## LINKI POKREWNE

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Nowe — AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)


