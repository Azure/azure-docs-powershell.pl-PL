---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: b1f4b8d53a1031cef76d51a87bbf9afa5b75758f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718717"
---
# Remove-AzureRmADSpCredential

## STRESZCZENIe
Usuwa poświadczenia z podmiotu zabezpieczeń usługi.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ObjectIdWithKeyIdParameterSet (domyślny)
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ObjectIdWithAllParameterSet
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithKeyIdParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithAllParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenia cmdlet Remove-AzureRmADSpCredential można użyć w celu usunięcia klucza poświadczeń z podmiotu zabezpieczeń usługi w przypadku złamania zabezpieczeń lub jako część wygaśnięcia przerzucania klucza poświadczeń.
Wartość główna usługi jest identyfikowana przez podanie identyfikatora obiektu lub głównej nazwy usługi (SPN).

Poświadczenie, które ma zostać usunięte, jest identyfikowane przez identyfikator klucza, jeśli pojedyncze poświadczenie ma zostać usunięte lub z przełącznikiem wszystkie, aby usunąć wszystkie poświadczenia skojarzone z podmiotem zabezpieczeń usługi.

## Przykłady

### --------------------------Przykład 1--------------------------
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

To polecenie usuwa klucz poświadczenia z podmiotu zabezpieczeń usługi.
W tym przykładzie klucz z identyfikatorem "9044423a-60a3-45ac-9ab1-09534157ebb" zostanie usunięty z podmiotu zabezpieczeń usługi.

### --------------------------Przykład 2--------------------------
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

To polecenie usuwa klucz poświadczenia z podmiotu zabezpieczeń usługi.
W tym przykładzie wszystkie poświadczenia zostaną usunięte z podmiotu zabezpieczeń usługi skojarzonego z główną nazwą usługi " http://test123 ".

## PARAMETRÓW

### -All
Przełącz, aby usunąć wszystkie poświadczenia skojarzone z podmiotem zabezpieczeń usługi.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Przełączanie do usuwania poświadczenia bez potwierdzenia.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
Określa klucz poświadczenia, który ma zostać usunięty.
Identyfikatory kluczy dla podmiotu usługi można uzyskać przy użyciu polecenia cmdlet Get-AzureRmADSpCredential.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Identyfikator obiektu podmiotu usługi, z którego mają zostać usunięte poświadczenia.

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Nazwa (SPN) podmiotu usługi, z którego mają zostać usunięte poświadczenia.

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

[Nowe — AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

