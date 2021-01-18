---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504043"
---
# <span data-ttu-id="426b9-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="426b9-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="426b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="426b9-102">SYNOPSIS</span></span>
<span data-ttu-id="426b9-103">Usuwa grupę hostów.</span><span class="sxs-lookup"><span data-stu-id="426b9-103">Removes a host group.</span></span>

## <span data-ttu-id="426b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="426b9-104">SYNTAX</span></span>

### <span data-ttu-id="426b9-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="426b9-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="426b9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="426b9-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="426b9-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="426b9-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="426b9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="426b9-108">DESCRIPTION</span></span>
<span data-ttu-id="426b9-109">To polecenie cmdlet spowoduje usunięcie grupy hostów</span><span class="sxs-lookup"><span data-stu-id="426b9-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="426b9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="426b9-110">EXAMPLES</span></span>

### <span data-ttu-id="426b9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="426b9-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="426b9-112">To polecenie pobiera i usuwa daną grupę hostów.</span><span class="sxs-lookup"><span data-stu-id="426b9-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="426b9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="426b9-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="426b9-114">To polecenie umożliwia usunięcie danej grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="426b9-114">This command removes the given host group.</span></span>

## <span data-ttu-id="426b9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="426b9-115">PARAMETERS</span></span>

### <span data-ttu-id="426b9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="426b9-116">-AsJob</span></span>
<span data-ttu-id="426b9-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="426b9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="426b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426b9-118">-DefaultProfile</span></span>
<span data-ttu-id="426b9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="426b9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="426b9-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="426b9-120">-InputObject</span></span>
<span data-ttu-id="426b9-121">Lokalny obiekt grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="426b9-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="426b9-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="426b9-122">-Name</span></span>
<span data-ttu-id="426b9-123">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="426b9-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="426b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="426b9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="426b9-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426b9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="426b9-126">-ResourceId</span></span>
<span data-ttu-id="426b9-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="426b9-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426b9-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="426b9-128">-Confirm</span></span>
<span data-ttu-id="426b9-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="426b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="426b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="426b9-130">-WhatIf</span></span>
<span data-ttu-id="426b9-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="426b9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="426b9-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="426b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="426b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426b9-133">CommonParameters</span></span>
<span data-ttu-id="426b9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="426b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426b9-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="426b9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426b9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="426b9-136">INPUTS</span></span>

### <span data-ttu-id="426b9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="426b9-137">System.String</span></span>

### <span data-ttu-id="426b9-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="426b9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="426b9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="426b9-139">OUTPUTS</span></span>

### <span data-ttu-id="426b9-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="426b9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="426b9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="426b9-141">NOTES</span></span>

## <span data-ttu-id="426b9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="426b9-142">RELATED LINKS</span></span>
