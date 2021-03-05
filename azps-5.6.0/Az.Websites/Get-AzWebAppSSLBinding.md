---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 08a9fbd9798a3fd3b53d7d71aca9ebd607d23164
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973697"
---
# Get-AzWebAppSSLBinding

## SYNOPSIS
Pobiera powiązanie SSL certyfikatu aplikacji Azure Web App.

## SKŁADNIA

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzWebAppSSLBinding** pobiera powiązanie Secure Sockets Layer (SSL) dla aplikacji Azure Web App.
Powiązania SSL służą do kojarzenia aplikacji Sieci Web z przekazanym certyfikatem.
Aplikacje Sieci Web mogą być powiązane z wieloma certyfikatami.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie powiązań SSL dla aplikacji sieci Web
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

To polecenie pobiera powiązania SSL dla aplikacji Sieci Web ContosoWebApp, która jest skojarzona z grupą zasobów ContosoResourceGroup.

### Przykład 2. Uzyskiwanie powiązań SSL dla aplikacji sieci Web za pomocą odwołania do obiektu
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

Polecenia w tym przykładzie również uzyskają powiązania SSL dla aplikacji sieci Web ContosoWebApp; Jednak w tym przypadku zamiast nazwy aplikacji Sieci Web i nazwy skojarzonej grupy zasobów jest używane odwołanie do obiektu.
To odwołanie do obiektu jest tworzone za pomocą pierwszego polecenia w tym przykładzie, które używa aplikacji **Get-AzWebApp** do utworzenia odwołania do obiektu do aplikacji Sieci Web o nazwie ContosoWebApp.
To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.
Ta zmienna i polecenie cmdlet **Get-AzWebAppSSLBinding** są następnie używane przez drugie polecenie do uzyskania powiązań SSL.

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

### — Nazwa
Określa nazwę powiązania SSL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do których jest przypisany certyfikat.
W tym samym *poleceniu nie można* użyć parametru ResourceGroupName ani *parametru WebApp.*

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Slot
Określa miejsce wdrożenia aplikacji Sieci Web.
Aby uzyskać miejsce wdrożenia, użyj Get-AzWebAppSlot cmdlet.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - WebApp
Określa aplikację sieci Web.
Aby uzyskać aplikację Sieci Web, użyj Get-AzWebApp cmdlet.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Określa nazwę aplikacji Sieci Web, z których to polecenie cmdlet pobiera powiązania SSL.
W tym samym poleceniu nie można użyć parametru *WebAppName* ani parametru *WebApp.*

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## NOTATKI

## LINKI POKREWNE

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


