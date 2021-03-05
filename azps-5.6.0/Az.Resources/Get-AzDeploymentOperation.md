---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 5507e180d5f56b75006f31f9cc6753f50d821a3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973610"
---
# Get-AzDeploymentOperation

## SYNOPSIS
Uzyskaj operację wdrażania

## SKŁADNIA

### GetByDeploymentName (domyślna)
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDeploymentOperation** zawiera listę wszystkich operacji, które były częścią wdrożenia, co pomaga w zidentyfikowaniu i podawać więcej informacji o dokładnie tych operacjach, które nie powiodły się w danym wdrożeniu.
Może też wyświetlać odpowiedź i zawartość żądania dla każdej operacji wdrażania.
Są to te same informacje, które podano w szczegółach wdrożenia w portalu.

Aby pobrać żądanie i zawartość odpowiedzi, włącz ustawienie podczas przesyłania wdrożenia za pomocą **programu New-AzDeployment.**
Może on potencjalnie rejestrować i ujawniać tajemnice, takie jak hasła używane we właściwości zasobu lub operacje **listKeys,** które są następnie zwracane po pobraniu operacji wdrażania.
Aby uzyskać więcej informacji na temat tego ustawienia i sposobu włączania go, zobacz New-AzDeployment i Debugowanie ARM wdrożeń szablonów

## PRZYKŁADY

### Przykład 1. Uzyskiwanie operacji wdrażania nadano nazwę wdrożenia
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

Pobiera operację wdrażania z nazwą "test" w zakresie bieżącej subskrypcji.

### Przykład 2. Uzyskiwanie wdrożenia i uzyskiwanie jego operacji wdrażania
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

To polecenie pobiera "test" wdrożenia w bieżącym zakresie subskrypcji i pobiera jego operacje wdrażania.

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

### -DeploymentName
Nazwa wdrożenia.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentObject
Obiekt wdrożenia.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperationId
Identyfikator operacji wdrażania.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Przed
Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation

## NOTATKI

## LINKI POKREWNE
