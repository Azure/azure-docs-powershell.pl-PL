---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178914"
---
# Get-AzADAppCredential

## SYNOPSIS
Pobiera listę poświadczeń skojarzonych z aplikacją.

## SKŁADNIA

### ApplicationObjectIdParameterSet (domyślne)
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Za Get-AzADAppCredential cmdlet można pobrać listę poświadczeń skojarzonych z aplikacją.
To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie poświadczeń aplikacji według identyfikatora obiektu

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu '1f99cf81-0146-4f4e-beae-2007d0668476'.

### Przykład 2. Uzyskiwanie poświadczeń aplikacji za pomocą rur

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

Pobiera aplikację z identyfikatorem obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i potokuje ją do polecenia cmdlet programu Get-AzADAppCredential w celu podania listy wszystkich poświadczeń dla tej aplikacji.

## PARAMETERS

### -ApplicationId
Identyfikator aplikacji, z których mają być pobierane poświadczenia.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
Obiekt aplikacji, z który mają być pobierane poświadczenia.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — DisplayName
Nazwa wyświetlana aplikacji.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Identyfikator obiektu aplikacji, z których mają być pobierane poświadczenia.

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Guid

### Microsoft.Azure.Commands.ActiveDirectory.PSADApplication

## OUTPUTS

### Microsoft.Azure.Commands.ActiveDirectory.PSADCredential

## NOTATKI

## LINKI POKREWNE

[New-AzadAppCredential](./New-AzADAppCredential.md)

[Remove-AzadAppCredential](./Remove-AzADAppCredential.md)

[Get-AzadApplication](./Get-AzADApplication.md)

