---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195426"
---
# Get-AzAccessToken

## SYNOPSIS
Pobierz nieprzetworzone token dostępu. Podczas korzystania z funkcji -ResourceUrl upewnij się, że wartość jest dopasowana do bieżącego środowiska platformy Azure. Możesz odwołać się do wartości `(Get-AzContext).Environment` .

## SKŁADNIA

### KnownResourceTypeName (Default)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Uzyskiwanie tokenu dostępu

## PRZYKŁADY

### Przykład 1. Uzyskiwanie tokenu dostępu nieprzetworzonego dla ARM końcowego
```powershell
PS C:\> Get-AzAccessToken
```

Uzyskiwanie tokenu dostępu dla punktu końcowego usługi ResourceManager dla bieżącego konta

### Przykład 2. Uzyskiwanie tokenu dostępu nieprzetworzonego dla punktu końcowego wykresu AAD
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Uzyskiwanie tokenu dostępu dla punktu końcowego wykresu AAD dla bieżącego konta

### Przykład 3. Uzyskiwanie tokenu dostępu nieprzetworzonego dla punktu końcowego wykresu AAD
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Uzyskiwanie tokenu dostępu punktu końcowego wykresu AAD dla bieżącego konta

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -ResourceTypeName
Opcjonalna nazwa typu ponownego użycia, obsługiwane wartości: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. Wartość domyślna to Arm, jeśli nie jest określona.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
Adres URL zasobu, do których żądasz tokenu, np. ' http://graph.windows.net/ '.

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - TenantId
Opcjonalny identyfikator dzierżawy. Użyj identyfikatora dzierżawy, jeśli nie określono kontekstu domyślnego.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## OUTPUTS

### System.String

## NOTATKI

## LINKI POKREWNE
