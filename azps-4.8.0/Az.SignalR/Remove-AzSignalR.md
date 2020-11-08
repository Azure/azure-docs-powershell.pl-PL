---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220350"
---
# <span data-ttu-id="460c5-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="460c5-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="460c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="460c5-102">SYNOPSIS</span></span>
<span data-ttu-id="460c5-103">Usuń usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="460c5-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="460c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="460c5-104">SYNTAX</span></span>

### <span data-ttu-id="460c5-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="460c5-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="460c5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="460c5-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="460c5-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="460c5-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="460c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="460c5-108">DESCRIPTION</span></span>
<span data-ttu-id="460c5-109">Usuń usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="460c5-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="460c5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="460c5-110">EXAMPLES</span></span>

### <span data-ttu-id="460c5-111">Usuwanie usługi sygnalizującej</span><span class="sxs-lookup"><span data-stu-id="460c5-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="460c5-112">Usuwanie wszystkich usług sygnalizacji z potoku</span><span class="sxs-lookup"><span data-stu-id="460c5-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="460c5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="460c5-113">PARAMETERS</span></span>

### <span data-ttu-id="460c5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="460c5-114">-AsJob</span></span>
<span data-ttu-id="460c5-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="460c5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="460c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460c5-116">-DefaultProfile</span></span>
<span data-ttu-id="460c5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="460c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="460c5-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="460c5-118">-InputObject</span></span>
<span data-ttu-id="460c5-119">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="460c5-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="460c5-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="460c5-120">-Name</span></span>
<span data-ttu-id="460c5-121">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="460c5-121">SignalR service name.</span></span>

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

### <span data-ttu-id="460c5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="460c5-122">-PassThru</span></span>
<span data-ttu-id="460c5-123">Zwraca wartość PRAWDA, Jeśli usunięcie zostało pomyślnie zrealizowane.</span><span class="sxs-lookup"><span data-stu-id="460c5-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="460c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="460c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="460c5-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="460c5-125">Resource group name.</span></span>

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

### <span data-ttu-id="460c5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="460c5-126">-ResourceId</span></span>
<span data-ttu-id="460c5-127">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="460c5-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="460c5-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="460c5-128">-Confirm</span></span>
<span data-ttu-id="460c5-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="460c5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="460c5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="460c5-130">-WhatIf</span></span>
<span data-ttu-id="460c5-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="460c5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="460c5-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="460c5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="460c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460c5-133">CommonParameters</span></span>
<span data-ttu-id="460c5-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="460c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460c5-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="460c5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460c5-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="460c5-136">INPUTS</span></span>

### <span data-ttu-id="460c5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="460c5-137">System.String</span></span>
### <span data-ttu-id="460c5-138">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="460c5-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="460c5-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="460c5-139">OUTPUTS</span></span>

### <span data-ttu-id="460c5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="460c5-140">System.Boolean</span></span>
## <span data-ttu-id="460c5-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="460c5-141">NOTES</span></span>

## <span data-ttu-id="460c5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="460c5-142">RELATED LINKS</span></span>
