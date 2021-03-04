---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 87a50c69449437401ff26b76b87cf0f334ab8d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975889"
---
# <span data-ttu-id="7132f-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="7132f-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="7132f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7132f-102">SYNOPSIS</span></span>
<span data-ttu-id="7132f-103">Usuwa usługę połączona z usługi Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7132f-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="7132f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7132f-104">SYNTAX</span></span>

### <span data-ttu-id="7132f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="7132f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7132f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7132f-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7132f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7132f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7132f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7132f-108">DESCRIPTION</span></span>
<span data-ttu-id="7132f-109">Polecenie Remove-AzDataFactoryV2LinkedService cmdlet usuwa usługę połączona z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7132f-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="7132f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7132f-110">EXAMPLES</span></span>

### <span data-ttu-id="7132f-111">Przykład 1. Usuwanie usługi połączonej</span><span class="sxs-lookup"><span data-stu-id="7132f-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="7132f-112">To polecenie usuwa usługę połączona o nazwie LinkedServiceTest z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7132f-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="7132f-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="7132f-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="7132f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7132f-114">PARAMETERS</span></span>

### <span data-ttu-id="7132f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7132f-115">-DataFactoryName</span></span>
<span data-ttu-id="7132f-116">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7132f-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7132f-117">To polecenie cmdlet usuwa usługę połączona z fabrycznych danych określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7132f-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7132f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7132f-118">-DefaultProfile</span></span>
<span data-ttu-id="7132f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7132f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7132f-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7132f-120">-Force</span></span>
<span data-ttu-id="7132f-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7132f-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7132f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7132f-122">-InputObject</span></span>
<span data-ttu-id="7132f-123">Określa obiekt LinkedService do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7132f-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7132f-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7132f-124">-Name</span></span>
<span data-ttu-id="7132f-125">Określa nazwę połączonej usługi do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7132f-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="7132f-126">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="7132f-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7132f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7132f-127">-ResourceGroupName</span></span>
<span data-ttu-id="7132f-128">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7132f-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7132f-129">To polecenie cmdlet usuwa usługę połączona z grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7132f-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7132f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7132f-130">-ResourceId</span></span>
<span data-ttu-id="7132f-131">Identyfikator zasobu Azure połączonej usługi do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7132f-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7132f-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7132f-132">-Confirm</span></span>
<span data-ttu-id="7132f-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7132f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7132f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7132f-134">-WhatIf</span></span>
<span data-ttu-id="7132f-135">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7132f-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7132f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7132f-136">CommonParameters</span></span>
<span data-ttu-id="7132f-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7132f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7132f-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7132f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7132f-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7132f-139">INPUTS</span></span>

### <span data-ttu-id="7132f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="7132f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="7132f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7132f-141">System.String</span></span>

## <span data-ttu-id="7132f-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7132f-142">OUTPUTS</span></span>

### <span data-ttu-id="7132f-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="7132f-143">System.Void</span></span>

## <span data-ttu-id="7132f-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7132f-144">NOTES</span></span>
<span data-ttu-id="7132f-145">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="7132f-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7132f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7132f-146">RELATED LINKS</span></span>

[<span data-ttu-id="7132f-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="7132f-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="7132f-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="7132f-148">Set-AzDataFactoryV2LinkedService</span></span>]()

