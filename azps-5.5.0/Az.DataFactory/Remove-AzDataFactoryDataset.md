---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186258"
---
# <span data-ttu-id="f5949-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f5949-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="f5949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5949-102">SYNOPSIS</span></span>
<span data-ttu-id="f5949-103">Usuwa zestaw danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f5949-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="f5949-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5949-104">SYNTAX</span></span>

### <span data-ttu-id="f5949-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="f5949-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5949-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f5949-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5949-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5949-107">DESCRIPTION</span></span>
<span data-ttu-id="f5949-108">Polecenie **cmdlet Remove-AzDataFactoryDataset** usuwa zestaw danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f5949-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="f5949-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5949-109">EXAMPLES</span></span>

### <span data-ttu-id="f5949-110">Przykład 1. Usuwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="f5949-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="f5949-111">To polecenie usuwa zestaw danych o nazwie DAWikiAggregatedData z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f5949-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="f5949-112">Polecenie zwróci wartość $True.</span><span class="sxs-lookup"><span data-stu-id="f5949-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="f5949-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5949-113">PARAMETERS</span></span>

### <span data-ttu-id="f5949-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5949-114">-DataFactory</span></span>
<span data-ttu-id="f5949-115">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="f5949-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f5949-116">To polecenie cmdlet usuwa zestaw danych z fabrycznej bazy danych, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="f5949-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5949-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f5949-117">-DataFactoryName</span></span>
<span data-ttu-id="f5949-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f5949-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f5949-119">To polecenie cmdlet usuwa zestaw danych z fabrycznych danych określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f5949-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5949-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5949-120">-DefaultProfile</span></span>
<span data-ttu-id="f5949-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f5949-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5949-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f5949-122">-Force</span></span>
<span data-ttu-id="f5949-123">Wskazuje, że to polecenie cmdlet usuwa zestaw danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f5949-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f5949-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5949-124">-Name</span></span>
<span data-ttu-id="f5949-125">Określa nazwę zestawu danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f5949-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5949-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5949-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5949-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f5949-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f5949-128">To polecenie cmdlet usuwa zestaw danych z grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f5949-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5949-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5949-129">-Confirm</span></span>
<span data-ttu-id="f5949-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f5949-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5949-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5949-131">-WhatIf</span></span>
<span data-ttu-id="f5949-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5949-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5949-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f5949-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5949-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5949-134">CommonParameters</span></span>
<span data-ttu-id="f5949-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5949-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5949-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5949-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5949-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5949-137">INPUTS</span></span>

### <span data-ttu-id="f5949-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f5949-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f5949-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f5949-139">System.String</span></span>

## <span data-ttu-id="f5949-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5949-140">OUTPUTS</span></span>

### <span data-ttu-id="f5949-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="f5949-141">System.Void</span></span>

## <span data-ttu-id="f5949-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5949-142">NOTES</span></span>
* <span data-ttu-id="f5949-143">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="f5949-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f5949-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5949-144">RELATED LINKS</span></span>

[<span data-ttu-id="f5949-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f5949-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="f5949-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f5949-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


