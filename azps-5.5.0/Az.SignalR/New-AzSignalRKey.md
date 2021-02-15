---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197802"
---
# <span data-ttu-id="b49a7-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="b49a7-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="b49a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b49a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b49a7-103">Ponownie wygeneruj klucz dostępu dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="b49a7-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="b49a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b49a7-104">SYNTAX</span></span>

### <span data-ttu-id="b49a7-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b49a7-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49a7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b49a7-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49a7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b49a7-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b49a7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b49a7-108">DESCRIPTION</span></span>
<span data-ttu-id="b49a7-109">Ponownie wygeneruj klucz dostępu dla usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="b49a7-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="b49a7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b49a7-110">EXAMPLES</span></span>

### <span data-ttu-id="b49a7-111">Ponowne generowanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="b49a7-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="b49a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b49a7-112">PARAMETERS</span></span>

### <span data-ttu-id="b49a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49a7-113">-DefaultProfile</span></span>
<span data-ttu-id="b49a7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b49a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b49a7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b49a7-115">-InputObject</span></span>
<span data-ttu-id="b49a7-116">Obiekt zasobu SignalR.</span><span class="sxs-lookup"><span data-stu-id="b49a7-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="b49a7-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b49a7-117">-KeyType</span></span>
<span data-ttu-id="b49a7-118">Typ klucza: podstawowy lub pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="b49a7-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="b49a7-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b49a7-119">-Name</span></span>
<span data-ttu-id="b49a7-120">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="b49a7-120">SignalR service name.</span></span>

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

### <span data-ttu-id="b49a7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b49a7-121">-PassThru</span></span>
<span data-ttu-id="b49a7-122">Zwraca wartość True (Prawda), jeśli pomyślnie ukończono błędy.</span><span class="sxs-lookup"><span data-stu-id="b49a7-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="b49a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="b49a7-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b49a7-124">Resource group name.</span></span>

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

### <span data-ttu-id="b49a7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b49a7-125">-ResourceId</span></span>
<span data-ttu-id="b49a7-126">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="b49a7-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="b49a7-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b49a7-127">-Confirm</span></span>
<span data-ttu-id="b49a7-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b49a7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b49a7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b49a7-129">-WhatIf</span></span>
<span data-ttu-id="b49a7-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b49a7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b49a7-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b49a7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b49a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49a7-132">CommonParameters</span></span>
<span data-ttu-id="b49a7-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b49a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49a7-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b49a7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49a7-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b49a7-135">INPUTS</span></span>

### <span data-ttu-id="b49a7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b49a7-136">System.String</span></span>
### <span data-ttu-id="b49a7-137">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b49a7-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="b49a7-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b49a7-138">OUTPUTS</span></span>

### <span data-ttu-id="b49a7-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b49a7-139">System.Boolean</span></span>
## <span data-ttu-id="b49a7-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b49a7-140">NOTES</span></span>

## <span data-ttu-id="b49a7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b49a7-141">RELATED LINKS</span></span>
