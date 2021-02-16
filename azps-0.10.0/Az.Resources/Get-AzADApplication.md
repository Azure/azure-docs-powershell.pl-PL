---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: a4d1831114db40295e30b30e0fb12621caff2c89
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398856"
---
# Get-AzADApplication

## SYNOPSIS
Lista istniejących aplikacji usługi Azure Active Directory.

## SKŁADNIA

### EmptyParameterSet (domyślne)
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### ApplicationObjectIdParameterSet
```
Get-AzADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdentifierUriParameterSet
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## OPIS
Lista istniejących aplikacji usługi Azure Active Directory.
Odnośnik aplikacji może być wykonywane przez obiekt ObjectId, ApplicationId, IdentyfikatorUri lub DisplayName.
Jeśli nie podano parametru, pobiera on wszystkie aplikacje w ramach dzierżawy.

## PRZYKŁADY

### Przykład 1. Lista wszystkich aplikacji

```
PS C:\> Get-AzADApplication
```

Wyświetla listę wszystkich aplikacji w ramach dzierżawy.

### Przykład 2. Lista aplikacji używających stronicowania

```
PS C:\> Get-AzADApplication -First 100
```

Wyświetla listę pierwszych 100 aplikacji w ramach dzierżawy.

### Przykład 3. Uzyskiwanie aplikacji za pomocą identyfikatora URI

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

Pobiera aplikację z identyfikatorem uri jako " http://mySecretApp1 ".

### Przykład 4. Uzyskiwanie aplikacji według identyfikatora obiektu

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

Pobiera aplikację o identyfikatorze obiektu "39e64ec6-569b-4030-8e1c-c3c519a05d69".

## PARAMETERS

### -ApplicationId
Identyfikator aplikacji do pobrania.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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

### -DisplayNameStartWith
Pobieraj wszystkie aplikacje, zaczynając od nazwy wyświetlanej.

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — najpierw
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

### -IdentifierUri
Unikatowy identyfikator Uri aplikacji w celu zdalnego dostępu.

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

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

### -ObjectId
Identyfikator obiektu aplikacji do pobrania.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.Guid

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication

## NOTATKI

## LINKI POKREWNE

[Remove-AzadAppCredential](./Remove-AzADAppCredential.md)

[New-AzadAppCredential](./New-AzADAppCredential.md)

[Get-AzadAppCredential](./Get-AzADAppCredential.md)

[Remove-AzadApplication](./Remove-AzADApplication.md)


[New-AzadApplication](./New-AzADApplication.md)

