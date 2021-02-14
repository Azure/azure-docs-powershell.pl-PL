---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244074"
---
# <span data-ttu-id="0c6a0-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0c6a0-101">Remove-AzHost</span></span>

## <span data-ttu-id="0c6a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6a0-103">Usuwa hosta.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-103">Removes a host.</span></span>

## <span data-ttu-id="0c6a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c6a0-104">SYNTAX</span></span>

### <span data-ttu-id="0c6a0-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0c6a0-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6a0-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="0c6a0-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c6a0-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="0c6a0-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c6a0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c6a0-108">DESCRIPTION</span></span>
<span data-ttu-id="0c6a0-109">To polecenie cmdlet spowoduje usunięcie hosta</span><span class="sxs-lookup"><span data-stu-id="0c6a0-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="0c6a0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c6a0-110">EXAMPLES</span></span>

### <span data-ttu-id="0c6a0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c6a0-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="0c6a0-112">To polecenie pobiera i usuwa danego hosta.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="0c6a0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0c6a0-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="0c6a0-114">To polecenie usuwa danego hosta.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-114">This command removes the given host.</span></span>

## <span data-ttu-id="0c6a0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c6a0-115">PARAMETERS</span></span>

### <span data-ttu-id="0c6a0-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0c6a0-116">-AsJob</span></span>
<span data-ttu-id="0c6a0-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0c6a0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c6a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6a0-118">-DefaultProfile</span></span>
<span data-ttu-id="0c6a0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6a0-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6a0-120">-HostGroupName</span></span>
<span data-ttu-id="0c6a0-121">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-121">The name of the host group.</span></span>

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

### <span data-ttu-id="0c6a0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c6a0-122">-InputObject</span></span>
<span data-ttu-id="0c6a0-123">Obiekt lokalny hosta.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-123">The local object of the host.</span></span>

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

### <span data-ttu-id="0c6a0-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0c6a0-124">-Name</span></span>
<span data-ttu-id="0c6a0-125">Nazwa hosta.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-125">The name of the host.</span></span>

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

### <span data-ttu-id="0c6a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c6a0-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c6a0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c6a0-128">-ResourceId</span></span>
<span data-ttu-id="0c6a0-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="0c6a0-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c6a0-130">-Confirm</span></span>
<span data-ttu-id="0c6a0-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6a0-132">-WhatIf</span></span>
<span data-ttu-id="0c6a0-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6a0-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6a0-135">CommonParameters</span></span>
<span data-ttu-id="0c6a0-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6a0-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c6a0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6a0-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c6a0-138">INPUTS</span></span>

### <span data-ttu-id="0c6a0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0c6a0-139">System.String</span></span>

### <span data-ttu-id="0c6a0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="0c6a0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="0c6a0-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c6a0-141">OUTPUTS</span></span>

### <span data-ttu-id="0c6a0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0c6a0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0c6a0-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c6a0-143">NOTES</span></span>

## <span data-ttu-id="0c6a0-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c6a0-144">RELATED LINKS</span></span>
