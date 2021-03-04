---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: b1d9aa1f212ce31a8bb7fadeff4e0ca8afcf05e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959313"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
Usuwa powiązanie SSL z przekazanego certyfikatu.

## SKŁADNIA

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Remove-AzWebAppSSLBinding** usuwa powiązanie Secure Sockets Layer (SSL) z aplikacji Azure Web App.
Powiązania SSL służą do kojarzenia aplikacji sieci Web z certyfikatem.

## PRZYKŁADY

### Przykład 1. Usuwanie powiązania SSL dla aplikacji sieci Web
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

To polecenie usuwa powiązanie SSL dla aplikacji sieci Web ContosoWebApp.
Ponieważ parametr *DeleteCertificate* nie jest uwzględniany, certyfikat zostanie usunięty, jeśli nie ma już żadnych powiązań SSL.

### Przykład 2. Usuwanie powiązania SSL bez usuwania certyfikatu
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Podobnie jak w przykładzie 1, to polecenie usuwa również powiązanie SSL dla aplikacji Sieci Web ContosoWebApp.
Jednak w tym przypadku parametr *DeleteCertificate* jest uwzględniany, a wartość parametru jest ustawiana jako $False.
Oznacza to, że certyfikat nie zostanie usunięty bez względu na to, czy ma jakiekolwiek powiązania SSL.

### Przykład 3. Usuwanie powiązania SSL za pomocą odwołania do obiektu
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

W tym przykładzie do usunięcia powiązania SSL dla aplikacji sieci Web jest używane odwołanie do obiektu witryny internetowej aplikacji sieci Web.
Pierwsze polecenie używa Get-AzWebApp cmdlet w celu utworzenia odwołania do obiektu aplikacji Sieci Web o nazwie ContosoWebApp.
To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.
Drugie polecenie używa odwołania do obiektu i polecenia **cmdlet Remove-AzWebAppSSLBinding** w celu usunięcia powiązania SSL.

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

### -DeleteCertificate
Określa akcję do podjęcia w przypadku usunięcia powiązania SSL jest jedynym powiązaniem używanym w certyfikacie.
Jeśli *wartość DeleteCertificate* $False, certyfikat nie zostanie usunięty po usunięciu powiązania.
Jeśli *wartość DeleteCertificate* $True lub nie jest zawarta w poleceniu, certyfikat zostanie usunięty wraz z powiązaniem SSL.
Certyfikat zostanie usunięty tylko w przypadku usunięcia powiązania SSL jest jedynym używanym w certyfikacie powiązaniem.
Jeśli certyfikat ma więcej niż jedno powiązanie, certyfikat nie zostanie usunięty niezależnie od wartości parametru *DeleteCertificate.*

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę aplikacji Sieci Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
Nie można użyć *parametru WebApp* w tym samym poleceniu co parametr *ResourceGroupName* i/lub *nazwa_sieci Web.*

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
Określa nazwę aplikacji Sieci Web.
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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## DANE WYJŚCIOWE

### System.Void

## NOTATKI

## LINKI POKREWNE

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppslot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


