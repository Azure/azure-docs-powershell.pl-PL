---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: a17f8e6457cc62799fdef3d3606e04962774fdac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955473"
---
# <span data-ttu-id="5bec4-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="5bec4-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="5bec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bec4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bec4-103">Ponownie wygeneruj klucz dostępu dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="5bec4-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="5bec4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5bec4-104">SYNTAX</span></span>

### <span data-ttu-id="5bec4-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5bec4-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bec4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bec4-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bec4-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bec4-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bec4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5bec4-108">DESCRIPTION</span></span>
<span data-ttu-id="5bec4-109">Ponownie wygeneruj klucz dostępu dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="5bec4-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="5bec4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5bec4-110">EXAMPLES</span></span>

### <span data-ttu-id="5bec4-111">Ponowne generowanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="5bec4-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="5bec4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bec4-112">PARAMETERS</span></span>

### <span data-ttu-id="5bec4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bec4-113">-DefaultProfile</span></span>
<span data-ttu-id="5bec4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bec4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bec4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bec4-115">-InputObject</span></span>
<span data-ttu-id="5bec4-116">Obiekt zasobu SignalR.</span><span class="sxs-lookup"><span data-stu-id="5bec4-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="5bec4-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5bec4-117">-KeyType</span></span>
<span data-ttu-id="5bec4-118">Typ klucza: podstawowy lub pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="5bec4-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bec4-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5bec4-119">-Name</span></span>
<span data-ttu-id="5bec4-120">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="5bec4-120">SignalR service name.</span></span>

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

### <span data-ttu-id="5bec4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bec4-121">-PassThru</span></span>
<span data-ttu-id="5bec4-122">Zwraca wartość True (Prawda), jeśli pomyślnie ukończono błędy.</span><span class="sxs-lookup"><span data-stu-id="5bec4-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="5bec4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bec4-123">-ResourceGroupName</span></span>
<span data-ttu-id="5bec4-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5bec4-124">Resource group name.</span></span>

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

### <span data-ttu-id="5bec4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bec4-125">-ResourceId</span></span>
<span data-ttu-id="5bec4-126">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="5bec4-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="5bec4-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bec4-127">-Confirm</span></span>
<span data-ttu-id="5bec4-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5bec4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bec4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bec4-129">-WhatIf</span></span>
<span data-ttu-id="5bec4-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bec4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bec4-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5bec4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bec4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bec4-132">CommonParameters</span></span>
<span data-ttu-id="5bec4-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bec4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bec4-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bec4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bec4-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bec4-135">INPUTS</span></span>

### <span data-ttu-id="5bec4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5bec4-136">System.String</span></span>
### <span data-ttu-id="5bec4-137">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="5bec4-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="5bec4-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bec4-138">OUTPUTS</span></span>

### <span data-ttu-id="5bec4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bec4-139">System.Boolean</span></span>
## <span data-ttu-id="5bec4-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5bec4-140">NOTES</span></span>

## <span data-ttu-id="5bec4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bec4-141">RELATED LINKS</span></span>
