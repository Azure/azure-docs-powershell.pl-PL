---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222640"
---
# <span data-ttu-id="a7a1d-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7a1d-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="a7a1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a1d-103">Usuwa fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-103">Removes a data factory.</span></span>

## <span data-ttu-id="a7a1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7a1d-104">SYNTAX</span></span>

### <span data-ttu-id="a7a1d-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a7a1d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a1d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a7a1d-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a1d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7a1d-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a1d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a7a1d-108">DESCRIPTION</span></span>
<span data-ttu-id="a7a1d-109">Polecenie cmdlet Remove-AzDataFactoryV2 powoduje usunięcie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="a7a1d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7a1d-110">EXAMPLES</span></span>

### <span data-ttu-id="a7a1d-111">Przykład 1: usuwanie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="a7a1d-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="a7a1d-112">To polecenie usuwa fabrykę danych o nazwie WikiADF z grupy zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="a7a1d-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="a7a1d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7a1d-114">PARAMETERS</span></span>

### <span data-ttu-id="a7a1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a1d-115">-DefaultProfile</span></span>
<span data-ttu-id="a7a1d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a1d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a7a1d-117">-Force</span></span>
<span data-ttu-id="a7a1d-118">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a7a1d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7a1d-119">-InputObject</span></span>
<span data-ttu-id="a7a1d-120">Określa obiekt DataFactory, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="a7a1d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a7a1d-121">-Name</span></span>
<span data-ttu-id="a7a1d-122">Określa nazwę fabryki danych, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="a7a1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7a1d-124">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a7a1d-125">To polecenie cmdlet umożliwia usunięcie fabryki danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7a1d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7a1d-126">-ResourceId</span></span>
<span data-ttu-id="a7a1d-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a7a1d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7a1d-128">-Confirm</span></span>
<span data-ttu-id="a7a1d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a1d-130">-WhatIf</span></span>
<span data-ttu-id="a7a1d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a7a1d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a1d-132">CommonParameters</span></span>
<span data-ttu-id="a7a1d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7a1d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a1d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a1d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a1d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7a1d-135">INPUTS</span></span>

### <span data-ttu-id="a7a1d-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a7a1d-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="a7a1d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a1d-137">System.String</span></span>

## <span data-ttu-id="a7a1d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7a1d-138">OUTPUTS</span></span>

### <span data-ttu-id="a7a1d-139">System. void</span><span class="sxs-lookup"><span data-stu-id="a7a1d-139">System.Void</span></span>

## <span data-ttu-id="a7a1d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7a1d-140">NOTES</span></span>
<span data-ttu-id="a7a1d-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="a7a1d-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a7a1d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7a1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="a7a1d-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7a1d-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="a7a1d-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7a1d-144">Set-AzDataFactoryV2</span></span>]()
