---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051886"
---
# Remove-AzWebAppSSLBinding

## STRESZCZENIe
Usuwa powiązanie SSL z przekazanego certyfikatu.

## POLECENIA

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

## Opis
Polecenie cmdlet **Remove-AzWebAppSSLBinding** usuwa powiązanie SSL (Secure Sockets Layer) z aplikacji Azure Web App.
Powiązania SSL są używane do kojarzenia aplikacji sieci Web z certyfikatem.

## Przykłady

### Przykład 1: Usuwanie powiązania SSL dla aplikacji sieci Web
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

To polecenie usuwa powiązanie SSL dla aplikacji sieci Web ContosoWebApp.
Ponieważ parametr *DeleteCertificate* nie jest uwzględniony, certyfikat zostanie usunięty, jeśli nie ma już żadnych powiązań SSL.

### Przykład 2: Usuwanie powiązania SSL bez usuwania certyfikatu
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Podobnie jak w przykładzie 1, to polecenie usuwa powiązanie SSL dla aplikacji sieci Web ContosoWebApp.
Jednak w tym przypadku jest uwzględniany parametr *DeleteCertificate* , a wartość parametru jest ustawiona na $false.
Oznacza to, że certyfikat nie zostanie usunięty bez względu na to, czy ma on jakiekolwiek powiązania SSL.

### Przykład 3: Usuwanie powiązania SSL za pomocą odwołania do obiektu
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

W tym przykładzie użyto odwołania do obiektu w witrynie sieci Web aplikacji w celu usunięcia powiązania SSL dla aplikacji sieci Web.
W pierwszym poleceniu użyto polecenia cmdlet Get-AzWebApp w celu utworzenia odwołania do obiektu dla aplikacji sieci Web o nazwie ContosoWebApp.
Odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.
Drugie polecenie używa odwołania do obiektu i polecenia cmdlet **Remove-AzWebAppSSLBinding** w celu usunięcia powiązania SSL.

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

### -DeleteCertificate
Określa działanie, które ma zostać wykonane, jeśli usunięte powiązanie SSL jest jedynym powiązaniem używanym przez certyfikat.
Jeśli *DeleteCertificate* jest ustawiona na $false, certyfikat nie zostanie usunięty, gdy powiązanie zostanie usunięte.
Jeśli *DeleteCertificate* jest ustawiona na $true lub nie jest uwzględniona w poleceniu, certyfikat zostanie usunięty wraz z powiązaniem SSL.
Certyfikat zostanie usunięty tylko wtedy, gdy usunięte powiązanie SSL jest jedynym powiązaniem używanym przez certyfikat.
Jeśli certyfikat zawiera więcej niż jedno powiązanie, certyfikat nie zostanie usunięty bez względu na wartość parametru *DeleteCertificate* .

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

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

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

### -Name (nazwa)
Określa nazwę aplikacji sieci Web.

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
Określa nazwę grupy zasobów, do której przypisano certyfikat.
Nie można użyć parametru *ResourceGroupName* i parametru *aplikacji* w tym samym poleceniu.

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

### -Slot
Określa miejsce wdrożenia aplikacji sieci Web.
Aby uzyskać miejsce do wdrożenia, użyj polecenia cmdlet Get-AzWebAppSlot.

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

### -Aplikacji
Określa aplikację sieci Web.
Aby uzyskać aplikację sieci Web, użyj polecenia cmdlet Get-AzWebApp.
Parametru *aplikacji* nie można używać w tym samym poleceniu, co parametr *ResourceGroupName* i/lub *WebAppName*.

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
Określa nazwę aplikacji sieci Web.
Nie można użyć parametru *WebAppName* i parametru *aplikacji* w tym samym poleceniu.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. webapps. modele. PSSite

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Nowe — AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


