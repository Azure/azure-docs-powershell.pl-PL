---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055058"
---
# Remove-AzureTrafficManagerEndpoint

## STRESZCZENIe
Umożliwia usunięcie punktu końcowego z profilu usługi Traffic Manager.

## POLECENIA

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureTrafficManagerEndpoint** umożliwia usunięcie punktu końcowego z profilu Microsoft Azure Traffic Manager.
Po usunięciu punktu końcowego przekazanie wyniku do polecenia cmdlet **Set-AzureTrafficManagerProfile** przy użyciu operatora potoku.
To polecenie cmdlet łączy się z usługą Azure, aby zapisać zmiany.

## Przykłady

### Przykład 1: Usuwanie punktu końcowego z profilu
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureTrafficManagerProfile** w celu uzyskania profilu o nazwie ContosoProfile, a następnie zapisanie go w zmiennej $TrafficManagerProfile.

Drugie polecenie usuwa punkt końcowy z nazwą domeny Contoso02App.cloudapp.net z profilu usługi Traffic Manager przechowywanego w $TrafficManagerProfile.
Polecenie przekazuje obiekt profilu do polecenia cmdlet **Set-AzureTrafficManagerProfile** , aby połączyć się z usługą Azure w celu zapisania zmian.

## PARAMETRÓW

### -NazwaDomeny
Określa nazwę domeny punktu końcowego, który ma zostać usunięty.

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

### -Force
```yaml
Type: SwitchParameter
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

### -TrafficManagerProfile
Określa obiekt profilu usługi Traffic Manager, z którego ma zostać usunięty punkt końcowy.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition
To polecenie cmdlet generuje obiekt profilu usługi Traffic Manager, który zawiera informacje na temat zaktualizowanego profilu.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


