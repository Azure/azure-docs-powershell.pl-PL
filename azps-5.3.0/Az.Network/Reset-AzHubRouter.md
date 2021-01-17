---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385133"
---
# <span data-ttu-id="de7b5-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="de7b5-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="de7b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="de7b5-103">Resetuje RoutingStatey zasobu VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="de7b5-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="de7b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de7b5-104">SYNTAX</span></span>

### <span data-ttu-id="de7b5-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de7b5-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de7b5-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="de7b5-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de7b5-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="de7b5-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de7b5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="de7b5-108">DESCRIPTION</span></span>
<span data-ttu-id="de7b5-109">Resetuje stan routingu istniejącego zasobu usługi VirtualHub tylko wtedy, gdy stan routingu wirtualnego centrum nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="de7b5-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="de7b5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de7b5-110">EXAMPLES</span></span>

### <span data-ttu-id="de7b5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de7b5-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="de7b5-112">Zresetuj stan routingu wirtualnego centrum przy użyciu jego ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="de7b5-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="de7b5-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="de7b5-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="de7b5-114">Zresetuj stan routingu koncentratora wirtualnego przy użyciu jego ResourceId.</span><span class="sxs-lookup"><span data-stu-id="de7b5-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="de7b5-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="de7b5-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="de7b5-116">Resetowanie stanu routingu wirtualnego centrum za pomocą obiektu wejścia.</span><span class="sxs-lookup"><span data-stu-id="de7b5-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="de7b5-117">Obiekt wejściowy jest typu PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="de7b5-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="de7b5-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="de7b5-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="de7b5-119">Istniejący wirtualny obiekt koncentratora może zostać pobrany, a następnie przekazany jako obiekt wejściowy w celu zresetowania — AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="de7b5-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="de7b5-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de7b5-120">PARAMETERS</span></span>

### <span data-ttu-id="de7b5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de7b5-121">-AsJob</span></span>
<span data-ttu-id="de7b5-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="de7b5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de7b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de7b5-123">-DefaultProfile</span></span>
<span data-ttu-id="de7b5-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de7b5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de7b5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="de7b5-125">-Force</span></span>
<span data-ttu-id="de7b5-126">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="de7b5-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="de7b5-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="de7b5-127">-InputObject</span></span>
<span data-ttu-id="de7b5-128">Wirtualny obiekt koncentratorowy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="de7b5-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de7b5-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de7b5-129">-Name</span></span>
<span data-ttu-id="de7b5-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="de7b5-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7b5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de7b5-131">-ResourceGroupName</span></span>
<span data-ttu-id="de7b5-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de7b5-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7b5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de7b5-133">-ResourceId</span></span>
<span data-ttu-id="de7b5-134">Identyfikator zasobu wirtualnego koncentratora, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="de7b5-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de7b5-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de7b5-135">-Confirm</span></span>
<span data-ttu-id="de7b5-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de7b5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de7b5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de7b5-137">-WhatIf</span></span>
<span data-ttu-id="de7b5-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de7b5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de7b5-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de7b5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de7b5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de7b5-140">CommonParameters</span></span>
<span data-ttu-id="de7b5-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de7b5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de7b5-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de7b5-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de7b5-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de7b5-143">INPUTS</span></span>

### <span data-ttu-id="de7b5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="de7b5-144">System.String</span></span>

### <span data-ttu-id="de7b5-145">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="de7b5-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="de7b5-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de7b5-146">OUTPUTS</span></span>

### <span data-ttu-id="de7b5-147">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="de7b5-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="de7b5-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de7b5-148">NOTES</span></span>

## <span data-ttu-id="de7b5-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de7b5-149">RELATED LINKS</span></span>

[<span data-ttu-id="de7b5-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="de7b5-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
