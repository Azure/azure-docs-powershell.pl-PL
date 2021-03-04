---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: c98b716f37fcf9aafafacdefad4c51b0451cf12d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955457"
---
# <span data-ttu-id="11771-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="11771-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="11771-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11771-102">SYNOPSIS</span></span>
<span data-ttu-id="11771-103">Uruchom ponownie usługę SignalR.</span><span class="sxs-lookup"><span data-stu-id="11771-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="11771-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11771-104">SYNTAX</span></span>

### <span data-ttu-id="11771-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="11771-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11771-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11771-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11771-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11771-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11771-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="11771-108">DESCRIPTION</span></span>
<span data-ttu-id="11771-109">Uruchom ponownie usługę SignalR.</span><span class="sxs-lookup"><span data-stu-id="11771-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="11771-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11771-110">EXAMPLES</span></span>

### <span data-ttu-id="11771-111">Ponowne uruchamianie określonej usługi SignalR</span><span class="sxs-lookup"><span data-stu-id="11771-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="11771-112">Domyślną grupę zasobów można ustawić za pomocą ustawienia \` Set-AzDefault -ResourceGroupName myResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="11771-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="11771-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11771-113">PARAMETERS</span></span>

### <span data-ttu-id="11771-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="11771-114">-AsJob</span></span>
<span data-ttu-id="11771-115">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="11771-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="11771-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11771-116">-DefaultProfile</span></span>
<span data-ttu-id="11771-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11771-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11771-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11771-118">-InputObject</span></span>
<span data-ttu-id="11771-119">Obiekt zasobu SignalR.</span><span class="sxs-lookup"><span data-stu-id="11771-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="11771-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11771-120">-Name</span></span>
<span data-ttu-id="11771-121">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="11771-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="11771-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11771-122">-PassThru</span></span>
<span data-ttu-id="11771-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="11771-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="11771-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11771-124">-ResourceGroupName</span></span>
<span data-ttu-id="11771-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11771-125">The resource group name.</span></span>
<span data-ttu-id="11771-126">Ustawienie domyślne będzie używane, jeśli nie zostanie określone.</span><span class="sxs-lookup"><span data-stu-id="11771-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="11771-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11771-127">-ResourceId</span></span>
<span data-ttu-id="11771-128">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="11771-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="11771-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11771-129">-Confirm</span></span>
<span data-ttu-id="11771-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11771-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11771-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11771-131">-WhatIf</span></span>
<span data-ttu-id="11771-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11771-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11771-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11771-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11771-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11771-134">CommonParameters</span></span>
<span data-ttu-id="11771-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11771-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11771-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11771-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11771-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11771-137">INPUTS</span></span>

### <span data-ttu-id="11771-138">System.String</span><span class="sxs-lookup"><span data-stu-id="11771-138">System.String</span></span>

### <span data-ttu-id="11771-139">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="11771-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="11771-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11771-140">OUTPUTS</span></span>

### <span data-ttu-id="11771-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11771-141">System.Boolean</span></span>

## <span data-ttu-id="11771-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11771-142">NOTES</span></span>

## <span data-ttu-id="11771-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11771-143">RELATED LINKS</span></span>
