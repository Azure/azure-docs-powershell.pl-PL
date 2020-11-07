---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: acd3fadd45dfc32c745af943013f4c0f00b663ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896345"
---
# <span data-ttu-id="2ff90-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2ff90-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="2ff90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ff90-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff90-103">Usuwa połączoną usługę z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="2ff90-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="2ff90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ff90-104">SYNTAX</span></span>

### <span data-ttu-id="2ff90-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2ff90-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff90-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ff90-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff90-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ff90-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff90-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2ff90-108">DESCRIPTION</span></span>
<span data-ttu-id="2ff90-109">Polecenie cmdlet Remove-AzDataFactoryV2LinkedService powoduje usunięcie połączonej usługi z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2ff90-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="2ff90-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ff90-110">EXAMPLES</span></span>

### <span data-ttu-id="2ff90-111">Przykład 1: usuwanie połączonej usługi</span><span class="sxs-lookup"><span data-stu-id="2ff90-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="2ff90-112">To polecenie powoduje usunięcie połączonej usługi o nazwie LinkedServiceTest z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2ff90-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="2ff90-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="2ff90-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="2ff90-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ff90-114">PARAMETERS</span></span>

### <span data-ttu-id="2ff90-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2ff90-115">-DataFactoryName</span></span>
<span data-ttu-id="2ff90-116">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="2ff90-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2ff90-117">To polecenie cmdlet umożliwia usunięcie połączonej usługi z fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2ff90-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ff90-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff90-118">-DefaultProfile</span></span>
<span data-ttu-id="2ff90-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff90-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ff90-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2ff90-120">-Force</span></span>
<span data-ttu-id="2ff90-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ff90-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2ff90-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2ff90-122">-InputObject</span></span>
<span data-ttu-id="2ff90-123">Określa obiekt LinkedService, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="2ff90-123">Specifies the LinkedService object to remove.</span></span>

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

### <span data-ttu-id="2ff90-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ff90-124">-Name</span></span>
<span data-ttu-id="2ff90-125">Określa nazwę połączonej usługi, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="2ff90-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="2ff90-126">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="2ff90-126">Name of the linked service.</span></span>

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

### <span data-ttu-id="2ff90-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff90-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ff90-128">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff90-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2ff90-129">To polecenie cmdlet powoduje usunięcie połączonej usługi z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2ff90-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ff90-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ff90-130">-ResourceId</span></span>
<span data-ttu-id="2ff90-131">Identyfikator zasobu platformy Azure połączonej usługi do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2ff90-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="2ff90-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ff90-132">-Confirm</span></span>
<span data-ttu-id="2ff90-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff90-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff90-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff90-134">-WhatIf</span></span>
<span data-ttu-id="2ff90-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff90-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2ff90-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff90-136">CommonParameters</span></span>
<span data-ttu-id="2ff90-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff90-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff90-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff90-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff90-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ff90-139">INPUTS</span></span>

### <span data-ttu-id="2ff90-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="2ff90-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="2ff90-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2ff90-141">System.String</span></span>

## <span data-ttu-id="2ff90-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ff90-142">OUTPUTS</span></span>

### <span data-ttu-id="2ff90-143">System. void</span><span class="sxs-lookup"><span data-stu-id="2ff90-143">System.Void</span></span>

## <span data-ttu-id="2ff90-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ff90-144">NOTES</span></span>
<span data-ttu-id="2ff90-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="2ff90-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2ff90-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ff90-146">RELATED LINKS</span></span>

[<span data-ttu-id="2ff90-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2ff90-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="2ff90-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2ff90-148">Set-AzDataFactoryV2LinkedService</span></span>]()

