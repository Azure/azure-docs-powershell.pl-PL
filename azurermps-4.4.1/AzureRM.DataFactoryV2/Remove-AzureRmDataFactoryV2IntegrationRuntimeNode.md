---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: e5bf7ca6951a78fc631b5bc2ffa96a2042423d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551900"
---
# <span data-ttu-id="fff55-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="fff55-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="fff55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fff55-102">SYNOPSIS</span></span>
<span data-ttu-id="fff55-103">Usuwanie węzła o podanej nazwie w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="fff55-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fff55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fff55-104">SYNTAX</span></span>

### <span data-ttu-id="fff55-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fff55-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="fff55-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fff55-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="fff55-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fff55-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fff55-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fff55-108">DESCRIPTION</span></span>
<span data-ttu-id="fff55-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntimeNode powoduje usunięcie węzła w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="fff55-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="fff55-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fff55-110">EXAMPLES</span></span>

### <span data-ttu-id="fff55-111">Przykład 1: Usuwanie węzła z środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="fff55-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="fff55-112">To polecenie usuwa węzeł o nazwie "Node_1" w środowisku wykonawczym integracji o nazwie "test-SelfHost-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="fff55-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="fff55-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fff55-113">PARAMETERS</span></span>

### <span data-ttu-id="fff55-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fff55-114">-Confirm</span></span>
<span data-ttu-id="fff55-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff55-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff55-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fff55-116">-DataFactoryName</span></span>
<span data-ttu-id="fff55-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="fff55-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff55-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fff55-118">-Force</span></span>
<span data-ttu-id="fff55-119">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fff55-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff55-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fff55-120">-InputObject</span></span>
<span data-ttu-id="fff55-121">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="fff55-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fff55-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="fff55-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="fff55-123">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fff55-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff55-124">-Nodename</span><span class="sxs-lookup"><span data-stu-id="fff55-124">-NodeName</span></span>
<span data-ttu-id="fff55-125">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fff55-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff55-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fff55-126">-ResourceGroupName</span></span>
<span data-ttu-id="fff55-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fff55-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff55-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fff55-128">-ResourceId</span></span>
<span data-ttu-id="fff55-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fff55-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff55-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff55-130">-WhatIf</span></span>
<span data-ttu-id="fff55-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff55-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="fff55-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fff55-132">INPUTS</span></span>

### <span data-ttu-id="fff55-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fff55-133">System.String</span></span>
<span data-ttu-id="fff55-134">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fff55-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="fff55-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fff55-135">OUTPUTS</span></span>

### <span data-ttu-id="fff55-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="fff55-136">System.Object</span></span>

## <span data-ttu-id="fff55-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fff55-137">NOTES</span></span>

## <span data-ttu-id="fff55-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fff55-138">RELATED LINKS</span></span>

