---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051691"
---
# Set-AzAttestationPolicy

## STRESZCZENIe
Ustawia zasady od dzierżawy na platformie Azure Attestationn.

## POLECENIA

### NameParameterSet
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Set-AzAttestationPolicy ustawia zasady od dzierżawy w zaświadczeniu platformy Azure.

## Przykłady

### Przykład 1
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

Ustawia zasady zdefiniowane przez użytkownika dla TEE typu *SgxEnclave* dla dostawcy zaświadczania *pshtest* przy użyciu formatu zasad tekstowych (domyślnie).

### Przykład 2
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

Ustawia zasady zdefiniowane przez użytkownika dla TEE typu *SgxEnclave* dla dostawcy zaświadczania *pshtest* przy użyciu formatu zasad JWT.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę dzierżawy.
To polecenie cmdlet ustawia zasady zaświadczania dla dzierżawy, którą ten parametr określa.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
To polecenie cmdlet domyślnie nie zwraca obiektu.
Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.

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

### -Policy
Określa dokument zasad, który należy ustawić.  Format zasad może być zarówno tekstowy, jak i tokenem w sieci Web JSON (JWT).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyFormat
Określa format zasady: text lub JWT (token internetowy JSON).  Domyślnym formatem zasad jest tekst.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów dla dostawcy zaświadczania.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Określa identyfikator zasobu dostawcy zaświadczania.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tee
Określa typ zaufanego środowiska wykonywania.
Obsługiwane są cztery typy środowiska: SgxEnclave, OpenEnclave, CyResComponent i VBSEnclave.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE
