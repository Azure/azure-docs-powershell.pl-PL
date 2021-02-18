---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181002"
---
# <span data-ttu-id="905cc-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="905cc-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="905cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="905cc-102">SYNOPSIS</span></span>
<span data-ttu-id="905cc-103">Usuwa fabryczne dane.</span><span class="sxs-lookup"><span data-stu-id="905cc-103">Removes a data factory.</span></span>

## <span data-ttu-id="905cc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="905cc-104">SYNTAX</span></span>

### <span data-ttu-id="905cc-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="905cc-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905cc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="905cc-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905cc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="905cc-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="905cc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="905cc-108">DESCRIPTION</span></span>
<span data-ttu-id="905cc-109">Polecenie Remove-AzDataFactoryV2 cmdlet usuwa fabryczne dane.</span><span class="sxs-lookup"><span data-stu-id="905cc-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="905cc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="905cc-110">EXAMPLES</span></span>

### <span data-ttu-id="905cc-111">Przykład 1. Usuwanie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="905cc-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="905cc-112">To polecenie usuwa z grupy zasobów o nazwie ADF fabryczne dane o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="905cc-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="905cc-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="905cc-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="905cc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="905cc-114">PARAMETERS</span></span>

### <span data-ttu-id="905cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905cc-115">-DefaultProfile</span></span>
<span data-ttu-id="905cc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="905cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="905cc-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="905cc-117">-Force</span></span>
<span data-ttu-id="905cc-118">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="905cc-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="905cc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="905cc-119">-InputObject</span></span>
<span data-ttu-id="905cc-120">Określa obiekt DataFactory do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="905cc-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="905cc-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="905cc-121">-Name</span></span>
<span data-ttu-id="905cc-122">Określa nazwę fabryki danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="905cc-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="905cc-124">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="905cc-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="905cc-125">To polecenie cmdlet usuwa grupę danych z grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="905cc-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="905cc-126">-ResourceId</span></span>
<span data-ttu-id="905cc-127">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="905cc-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="905cc-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="905cc-128">-Confirm</span></span>
<span data-ttu-id="905cc-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="905cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="905cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="905cc-130">-WhatIf</span></span>
<span data-ttu-id="905cc-131">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="905cc-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="905cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905cc-132">CommonParameters</span></span>
<span data-ttu-id="905cc-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905cc-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905cc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905cc-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="905cc-135">INPUTS</span></span>

### <span data-ttu-id="905cc-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="905cc-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="905cc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="905cc-137">System.String</span></span>

## <span data-ttu-id="905cc-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="905cc-138">OUTPUTS</span></span>

### <span data-ttu-id="905cc-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="905cc-139">System.Void</span></span>

## <span data-ttu-id="905cc-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="905cc-140">NOTES</span></span>
<span data-ttu-id="905cc-141">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="905cc-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="905cc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="905cc-142">RELATED LINKS</span></span>

[<span data-ttu-id="905cc-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="905cc-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="905cc-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="905cc-144">Set-AzDataFactoryV2</span></span>]()
