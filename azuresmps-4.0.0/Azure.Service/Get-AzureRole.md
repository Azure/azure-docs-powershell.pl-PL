---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055280"
---
# Get-AzureRole

## STRESZCZENIe
Zwraca listę ról w usłudze Microsoft Azure.

## POLECENIA

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRole** zwraca obiekt listy ze szczegółami dotyczącymi ról w usłudze Microsoft Azure.
Jeśli określisz parametr *rolename* , funkcja **Get-AzureRole** zwraca dane tylko w ramach tej roli.
Jeśli określisz parametr *InstanceDetails* , zostaną zwrócone dodatkowe szczegóły dotyczące wystąpienia.

## Przykłady

### Przykład 1: uzyskiwanie listy ról dla usługi
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

To polecenie zwraca obiekt ze szczegółami dotyczącymi wszystkich ról produkcyjnych uruchomionych w usłudze MySvc01.

### Przykład 2: uzyskiwanie szczegółowych informacji na temat roli działającej w usłudze
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

To polecenie zwraca obiekt ze szczegółami dotyczącymi roli MyTestVM3, działając w środowisku przemieszczania usługi MySvc01.

### Przykład 3: uzyskiwanie informacji o wystąpieniu dla wystąpień roli uruchomionych w usłudze
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

To polecenie zwraca obiekt ze szczegółami dotyczącymi wystąpień roli MyTestVM02 działającej w środowisku produkcyjnym w usłudze MySvc01.

### Przykład 4: uzyskiwanie tabeli wystąpień ról skojarzonych z usługą
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

To polecenie zwraca tabelę z nazwą wystąpienia, rozmiarem i stanem wszystkich wystąpień ról uruchomionych w środowisku produkcyjnym w usłudze MySvc01.

## PARAMETRÓW

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceDetails
Określa, że to polecenie cmdlet zwraca szczegóły dotyczące wystąpień poszczególnych ról.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -Rolename
Określa nazwę roli, którą należy uzyskać.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Określa nazwę usługi platformy Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Określa środowisko wdrażania platformy Azure.
Dopuszczalne wartości tego parametru to: production lub Staging.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureRole](./Set-AzureRole.md)


