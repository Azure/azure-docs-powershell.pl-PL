---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891926"
---
# Get-AzWebAppSSLBinding

## STRESZCZENIe
Pobiera powiązanie SSL certyfikatu aplikacji Azure Web App.

## POLECENIA

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzWebAppSSLBinding** Pobiera powiązanie SSL (Secure Sockets Layer) dla aplikacji Azure Web App.
Powiązania SSL są używane do kojarzenia aplikacji sieci Web z przekazanym certyfikatem.
Aplikacje sieci Web mogą być powiązane z wieloma certyfikatami.

## Przykłady

### Przykład 1: uzyskiwanie powiązań SSL dla aplikacji sieci Web
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

To polecenie pobiera powiązania protokołu SSL dla aplikacji sieci Web ContosoWebApp, która jest skojarzona z grupą zasobów ContosoResourceGroup.

### Przykład 2: używanie odwołania do obiektu w celu uzyskania powiązań SSL dla aplikacji sieci Web
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

Polecenia w tym przykładzie uzyskują również powiązania SSL dla aplikacji sieci Web ContosoWebApp; Jednak w tym przypadku zamiast nazwy aplikacji sieci Web i nazwy skojarzonej grupy zasobów zostanie użyte odwołanie do obiektu.
To odwołanie do obiektu jest tworzone przez pierwsze polecenie w przykładzie, w którym użyto polecenia **Get-AzWebApp** w celu utworzenia odwołania do obiektu do aplikacji sieci Web o nazwie ContosoWebApp.
Odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.

Ta zmienna i polecenie cmdlet **Get-AzWebAppSSLBinding** są następnie używane przez drugie polecenie w celu uzyskania powiązań SSL.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę powiązania SSL.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której przypisano certyfikat.

Nie można użyć parametru *ResourceGroupName* i parametru *aplikacji* w tym samym poleceniu.

```yaml
Type: String
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
Type: String
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

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Określa nazwę aplikacji sieci Web, z której to polecenie cmdlet pobiera powiązania SSL.

Nie można użyć parametru *WebAppName* i parametru *aplikacji* w tym samym poleceniu.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Klienta
Parametr "aplikacji" akceptuje wartość typu "site" z procesu

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


