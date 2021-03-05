---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 21c623187e72406d1120e225bf567a48bb2e6f30
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983313"
---
# <span data-ttu-id="a161b-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a161b-101">Remove-AzHost</span></span>

## <span data-ttu-id="a161b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a161b-102">SYNOPSIS</span></span>
<span data-ttu-id="a161b-103">Usuwa hosta.</span><span class="sxs-lookup"><span data-stu-id="a161b-103">Removes a host.</span></span>

## <span data-ttu-id="a161b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a161b-104">SYNTAX</span></span>

### <span data-ttu-id="a161b-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a161b-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a161b-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="a161b-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a161b-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="a161b-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a161b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a161b-108">DESCRIPTION</span></span>
<span data-ttu-id="a161b-109">To polecenie cmdlet spowoduje usunięcie hosta</span><span class="sxs-lookup"><span data-stu-id="a161b-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="a161b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a161b-110">EXAMPLES</span></span>

### <span data-ttu-id="a161b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a161b-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="a161b-112">To polecenie pobiera i usuwa danego hosta.</span><span class="sxs-lookup"><span data-stu-id="a161b-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="a161b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a161b-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="a161b-114">To polecenie usuwa danego hosta.</span><span class="sxs-lookup"><span data-stu-id="a161b-114">This command removes the given host.</span></span>

## <span data-ttu-id="a161b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a161b-115">PARAMETERS</span></span>

### <span data-ttu-id="a161b-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a161b-116">-AsJob</span></span>
<span data-ttu-id="a161b-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a161b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a161b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a161b-118">-DefaultProfile</span></span>
<span data-ttu-id="a161b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a161b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a161b-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="a161b-120">-HostGroupName</span></span>
<span data-ttu-id="a161b-121">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="a161b-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a161b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a161b-122">-InputObject</span></span>
<span data-ttu-id="a161b-123">Obiekt lokalny hosta.</span><span class="sxs-lookup"><span data-stu-id="a161b-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a161b-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a161b-124">-Name</span></span>
<span data-ttu-id="a161b-125">Nazwa hosta.</span><span class="sxs-lookup"><span data-stu-id="a161b-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a161b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a161b-126">-ResourceGroupName</span></span>
<span data-ttu-id="a161b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a161b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a161b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a161b-128">-ResourceId</span></span>
<span data-ttu-id="a161b-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a161b-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="a161b-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a161b-130">-Confirm</span></span>
<span data-ttu-id="a161b-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a161b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a161b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a161b-132">-WhatIf</span></span>
<span data-ttu-id="a161b-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a161b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a161b-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a161b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a161b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a161b-135">CommonParameters</span></span>
<span data-ttu-id="a161b-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a161b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a161b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a161b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a161b-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a161b-138">INPUTS</span></span>

### <span data-ttu-id="a161b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a161b-139">System.String</span></span>

### <span data-ttu-id="a161b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="a161b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="a161b-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a161b-141">OUTPUTS</span></span>

### <span data-ttu-id="a161b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a161b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a161b-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a161b-143">NOTES</span></span>

## <span data-ttu-id="a161b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a161b-144">RELATED LINKS</span></span>
