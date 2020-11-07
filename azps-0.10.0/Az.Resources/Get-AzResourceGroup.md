---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: d09031270e61be80228003ae2a9ae47a5ce5ac74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892570"
---
# Get-AzResourceGroup

## STRESZCZENIe
Pobiera grupy zasobów.

## POLECENIA

### GetByResourceGroupName (domyślny)
```
Get-AzResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzResourceGroup** umożliwia pobieranie grup zasobów platformy Azure w bieżącej subskrypcji.
Możesz uzyskać dostęp do wszystkich grup zasobów lub określić grupę zasobów według nazwy lub według innych właściwości.
Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich grup zasobów w bieżącej subskrypcji.
Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzResourceGroup.

## Przykłady

### Przykład 1: pobieranie grupy zasobów według nazwy
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

To polecenie pobiera grupę zasobów platformy Azure w ramach abonamentu o nazwie EngineerBlog.

### Przykład 2: pobieranie wszystkich tagów grupy zasobów
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

To polecenie pobiera grupę zasobów o nazwie ContosoRG i wyświetla znaczniki skojarzone z tą grupą.

### Przykład 3: wyświetlanie grup zasobów według lokalizacji
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Przykład 4: wyświetlanie nazw wszystkich grup zasobów w określonej lokalizacji
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Przykład 5: wyświetlanie grup zasobów, których nazwy zaczynają się od serwera WebServer
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

## PARAMETRÓW

### -ApiVersion
Określa wersję API obsługiwaną przez dostawcę zasobów.
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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -ID
Określa identyfikator grupy zasobów, którą należy pobrać.
Znaki wieloznaczne są niedozwolone.

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
Określa lokalizację grupy zasobów, którą należy pobrać.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę grupy zasobów, którą należy pobrać. Ten parametr obsługuje symbole wieloznaczne na początku i/lub końcu ciągu.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.

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

### -Tag
Tag Hashtable w celu filtrowania grup zasobów według.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)


