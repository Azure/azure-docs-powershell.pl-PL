---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186467"
---
# Get-AzResourceGroup

## SYNOPSIS
Pobiera grupy zasobów.

## SKŁADNIA

### GetByResourceGroupName (Domyślna)
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzResourceGroup** pobiera grupy zasobów platformy Azure w bieżącej subskrypcji.
Możesz pobrać wszystkie grupy zasobów lub określić grupę zasobów według nazwy lub innych właściwości.
Domyślnie to polecenie cmdlet pobiera wszystkie grupy zasobów w bieżącej subskrypcji.
Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz New-AzResourceGroup cmdlet.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie grupy zasobów według nazwy
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

To polecenie pobiera grupę zasobów platformy Azure w ramach subskrypcji o nazwie EngineerBlog.

### Przykład 2. Uzyskiwanie wszystkich tagów grupy zasobów
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

To polecenie pobiera grupę zasobów o nazwie ContosoRG i wyświetla skojarzone z nią tagi.

### Przykład 3. Uzyskiwanie grup zasobów na podstawie tagu
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### Przykład 4. Wyświetlanie grup zasobów według lokalizacji
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Przykład 5. Wyświetlanie nazw wszystkich grup zasobów w określonej lokalizacji
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Przykład 6. Wyświetlanie grup zasobów, których nazwy zaczynają się od serwera sieci Web
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## PARAMETERS

### -ApiVersion
Określa wersję interfejsu API obsługiwaną przez dostawcę zasobów.
Możesz określić inną wersję niż wersja domyślna.

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

### — Identyfikator
Określa identyfikator grupy zasobów do uzyskania.
Symbole wieloznaczne są niedozwolone.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację grupy zasobów do uzyskania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę grupy zasobów do uzyskania. Ten parametr obsługuje symbole wieloznaczne na początku i/lub na końcu ciągu.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### — Przed
Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.

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

### — Tag
Tabela skrótów tagów, według których można filtrować grupy zasobów.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Collections.Hashtable

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroup

## NOTATKI

## LINKI POKREWNE

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)

