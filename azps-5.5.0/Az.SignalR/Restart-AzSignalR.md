---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242067"
---
# <span data-ttu-id="7405f-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="7405f-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="7405f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7405f-102">SYNOPSIS</span></span>
<span data-ttu-id="7405f-103">Uruchom ponownie usługę SignalR.</span><span class="sxs-lookup"><span data-stu-id="7405f-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="7405f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7405f-104">SYNTAX</span></span>

### <span data-ttu-id="7405f-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7405f-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7405f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7405f-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7405f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7405f-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7405f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7405f-108">DESCRIPTION</span></span>
<span data-ttu-id="7405f-109">Uruchom ponownie usługę SignalR.</span><span class="sxs-lookup"><span data-stu-id="7405f-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="7405f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7405f-110">EXAMPLES</span></span>

### <span data-ttu-id="7405f-111">Ponowne uruchamianie określonej usługi SignalR</span><span class="sxs-lookup"><span data-stu-id="7405f-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="7405f-112">Domyślną grupę zasobów można ustawić za pomocą ustawienia \` Set-AzDefault -ResourceGroupName myResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="7405f-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="7405f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7405f-113">PARAMETERS</span></span>

### <span data-ttu-id="7405f-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7405f-114">-AsJob</span></span>
<span data-ttu-id="7405f-115">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="7405f-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="7405f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7405f-116">-DefaultProfile</span></span>
<span data-ttu-id="7405f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7405f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7405f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7405f-118">-InputObject</span></span>
<span data-ttu-id="7405f-119">Obiekt zasobu SignalR.</span><span class="sxs-lookup"><span data-stu-id="7405f-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="7405f-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7405f-120">-Name</span></span>
<span data-ttu-id="7405f-121">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="7405f-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="7405f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7405f-122">-PassThru</span></span>
<span data-ttu-id="7405f-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7405f-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7405f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7405f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7405f-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7405f-125">The resource group name.</span></span>
<span data-ttu-id="7405f-126">Ustawienie domyślne będzie używane, jeśli nie zostanie określone.</span><span class="sxs-lookup"><span data-stu-id="7405f-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="7405f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7405f-127">-ResourceId</span></span>
<span data-ttu-id="7405f-128">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="7405f-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7405f-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7405f-129">-Confirm</span></span>
<span data-ttu-id="7405f-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7405f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7405f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7405f-131">-WhatIf</span></span>
<span data-ttu-id="7405f-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7405f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7405f-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7405f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7405f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7405f-134">CommonParameters</span></span>
<span data-ttu-id="7405f-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7405f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7405f-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7405f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7405f-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7405f-137">INPUTS</span></span>

### <span data-ttu-id="7405f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7405f-138">System.String</span></span>

### <span data-ttu-id="7405f-139">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7405f-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="7405f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7405f-140">OUTPUTS</span></span>

### <span data-ttu-id="7405f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7405f-141">System.Boolean</span></span>

## <span data-ttu-id="7405f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7405f-142">NOTES</span></span>

## <span data-ttu-id="7405f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7405f-143">RELATED LINKS</span></span>
