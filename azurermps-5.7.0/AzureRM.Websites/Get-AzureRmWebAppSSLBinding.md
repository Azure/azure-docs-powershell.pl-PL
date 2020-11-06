---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: c2780b05e6caae6e200e7fbab26f02a6644f9ebc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526478"
---
# Get-AzureRmWebAppSSLBinding

## STRESZCZENIe
Pobiera powiązanie SSL certyfikatu aplikacji Azure Web App.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### S1
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmWebAppSSLBinding** Pobiera powiązanie SSL (Secure Sockets Layer) dla aplikacji Azure Web App.
Powiązania SSL są używane do kojarzenia aplikacji sieci Web z przekazanym certyfikatem.
Aplikacje sieci Web mogą być powiązane z wieloma certyfikatami.

## Przykłady

### Przykład 1: uzyskiwanie powiązań SSL dla aplikacji sieci Web
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

To polecenie pobiera powiązania protokołu SSL dla aplikacji sieci Web ContosoWebApp, która jest skojarzona z grupą zasobów ContosoResourceGroup.

### Przykład 2: używanie odwołania do obiektu w celu uzyskania powiązań SSL dla aplikacji sieci Web
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

Polecenia w tym przykładzie uzyskują również powiązania SSL dla aplikacji sieci Web ContosoWebApp; Jednak w tym przypadku zamiast nazwy aplikacji sieci Web i nazwy skojarzonej grupy zasobów zostanie użyte odwołanie do obiektu.
To odwołanie do obiektu jest tworzone przez pierwsze polecenie w przykładzie, w którym użyto polecenia **Get-AzureRmWebApp** w celu utworzenia odwołania do obiektu do aplikacji sieci Web o nazwie ContosoWebApp.
Odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.

Ta zmienna i polecenie cmdlet **Get-AzureRmWebAppSSLBinding** są następnie używane przez drugie polecenie w celu uzyskania powiązań SSL.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Aby uzyskać miejsce do wdrożenia, użyj polecenia cmdlet Get-AzureRMWebAppSlot.

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
Aby uzyskać aplikację sieci Web, użyj polecenia cmdlet Get-AzureRmWebApp.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Klienta
Parametr "aplikacji" akceptuje wartość typu "site" z procesu

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Remove-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


