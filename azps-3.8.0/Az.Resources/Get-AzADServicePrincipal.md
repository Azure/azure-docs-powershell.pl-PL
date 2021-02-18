---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 45f355b0317d8db8f9f24b40d5161e38888c4bb3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405588"
---
# Get-AzADServicePrincipal

## SYNOPSIS
Filtruje podmioty zabezpieczeń usługi Active Directory.

## SKŁADNIA

### EmptyParameterSet (domyślne)
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## OPIS
Filtruje podmioty zabezpieczeń usługi Active Directory.

## PRZYKŁADY

### Przykład 1. Lista głównych podmiotów usługi AD

```
PS C:\> Get-AzADServicePrincipal
```

Wyświetla listę wszystkich głównych podmiotów usługi AD w dzierżawie.

### Przykład 2. Lista głównych podmiotów usługi AD przy użyciu stronicowania

```
PS C:\> Get-AzADServicePrincipal -First 100
```

Wyświetla listę pierwszych 100 głównych podmiotów usługi AD w dzierżawie.

### Przykład 3. Lista głównych podmiotów usługi według sieci SPN

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

Wyświetla listę głównych podmiotów usługi ze spN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.

### Przykład 4. Lista podmiotów zabezpieczeń usługi według ciągu wyszukiwania

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

Wyświetla listę wszystkich głównych podmiotów usługi AD, których nazwa wyświetlana zaczyna się od "sieci Web".

### Przykład 5. Lista głównych podmiotów zabezpieczeń usług za pomocą rur

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

Pobiera aplikację USŁUGI AD z identyfikatorem obiektu "39e64ec6-569b-4030-8e1c-c3c519a05d69" i potokuje ją do polecenia cmdlet programu Get-AzADServicePrincipal, aby wyświetlić listę wszystkich głównych podmiotów usługi dla tej aplikacji.

## PARAMETERS

### -ApplicationId
Identyfikator aplikacji podmiotu zabezpieczeń usługi.

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
Obiekt aplikacji, którego podmiot zabezpieczeń usługi jest pobierany.

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
Nazwa wyświetlana podmiotu zabezpieczeń usługi.

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

### -DisplayNameBeginsWith
Ciąg wyszukiwania podmiotu zabezpieczeń usługi.

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Identyfikator obiektu podmiotu zabezpieczeń usługi.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
SpN usługi.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - IncludeTotalCount
Raportuje liczbę obiektów w zestawie danych. Obecnie ten parametr nie działa nic.

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

### — Pomiń
Ignoruje pierwsze obiekty N, a następnie pobiera pozostałe obiekty.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Najpierw
Maksymalna liczba obiektów, które mają być zwracane.

```yaml
Type: System.UInt64
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

### System.String

### System.Guid

### Microsoft.Azure.Commands.ActiveDirectory.PSADApplication

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

## NOTATKI

## LINKI POKREWNE

[New-AzadServicePrincipal](./New-AzADServicePrincipal.md)


[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzadApplication](./Get-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

