---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 067dd93f28a5019de96f146a237fe131a9717bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955466"
---
# <span data-ttu-id="3b956-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="3b956-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="3b956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b956-102">SYNOPSIS</span></span>
<span data-ttu-id="3b956-103">Usuwanie usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="3b956-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="3b956-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3b956-104">SYNTAX</span></span>

### <span data-ttu-id="3b956-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3b956-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b956-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b956-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b956-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b956-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b956-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3b956-108">DESCRIPTION</span></span>
<span data-ttu-id="3b956-109">Usuwanie usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="3b956-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="3b956-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3b956-110">EXAMPLES</span></span>

### <span data-ttu-id="3b956-111">Usuwanie usługi SignalR</span><span class="sxs-lookup"><span data-stu-id="3b956-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="3b956-112">Usuwanie całej usługi SignalR z potoku</span><span class="sxs-lookup"><span data-stu-id="3b956-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="3b956-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b956-113">PARAMETERS</span></span>

### <span data-ttu-id="3b956-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3b956-114">-AsJob</span></span>
<span data-ttu-id="3b956-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3b956-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b956-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b956-116">-DefaultProfile</span></span>
<span data-ttu-id="3b956-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b956-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b956-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b956-118">-InputObject</span></span>
<span data-ttu-id="3b956-119">Obiekt zasobu SignalR.</span><span class="sxs-lookup"><span data-stu-id="3b956-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b956-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3b956-120">-Name</span></span>
<span data-ttu-id="3b956-121">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="3b956-121">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b956-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b956-122">-PassThru</span></span>
<span data-ttu-id="3b956-123">Zwraca wartość True (Prawda), jeśli usunięcie zostało ukończone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="3b956-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b956-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b956-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b956-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b956-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b956-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b956-126">-ResourceId</span></span>
<span data-ttu-id="3b956-127">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="3b956-127">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b956-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b956-128">-Confirm</span></span>
<span data-ttu-id="3b956-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b956-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b956-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b956-130">-WhatIf</span></span>
<span data-ttu-id="3b956-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b956-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b956-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3b956-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b956-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b956-133">CommonParameters</span></span>
<span data-ttu-id="3b956-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b956-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b956-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b956-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b956-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b956-136">INPUTS</span></span>

### <span data-ttu-id="3b956-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3b956-137">System.String</span></span>
### <span data-ttu-id="3b956-138">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="3b956-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="3b956-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b956-139">OUTPUTS</span></span>

### <span data-ttu-id="3b956-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b956-140">System.Boolean</span></span>
## <span data-ttu-id="3b956-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3b956-141">NOTES</span></span>

## <span data-ttu-id="3b956-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b956-142">RELATED LINKS</span></span>
