---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 2261e3e0f9237985459dc69e06ba4f055dd86427
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962666"
---
# <span data-ttu-id="b6b06-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="b6b06-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="b6b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6b06-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b06-103">Resetuje zasób VirtualHub stan routingu.</span><span class="sxs-lookup"><span data-stu-id="b6b06-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="b6b06-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6b06-104">SYNTAX</span></span>

### <span data-ttu-id="b6b06-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b6b06-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b06-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b06-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b06-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b6b06-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b06-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6b06-108">DESCRIPTION</span></span>
<span data-ttu-id="b6b06-109">Resetuje stan routingu istniejącego zasobu aplikacji VirtualHub tylko wtedy, gdy stan routingu centrum wirtualnego nie jest aprowowany.</span><span class="sxs-lookup"><span data-stu-id="b6b06-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="b6b06-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6b06-110">EXAMPLES</span></span>

### <span data-ttu-id="b6b06-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6b06-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="b6b06-112">Zresetuj stan routingu centrum wirtualnego za pomocą jego nazwa_grupy zasobów i nazwa_zasobu.</span><span class="sxs-lookup"><span data-stu-id="b6b06-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="b6b06-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b6b06-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="b6b06-114">Zresetuj stan routingu centrum wirtualnego przy użyciu jego zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b6b06-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="b6b06-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b6b06-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="b6b06-116">Zresetuj stan routingu centrum wirtualnego przy użyciu obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="b6b06-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="b6b06-117">Obiekt wejściowy jest typu PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b6b06-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="b6b06-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b6b06-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="b6b06-119">Istniejący obiekt centrum wirtualnego może zostać pobrany, a następnie przekazany jako obiekt wejściowy do środowiska Reset-AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="b6b06-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="b6b06-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6b06-120">PARAMETERS</span></span>

### <span data-ttu-id="b6b06-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b6b06-121">-AsJob</span></span>
<span data-ttu-id="b6b06-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b6b06-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6b06-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b06-123">-DefaultProfile</span></span>
<span data-ttu-id="b6b06-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b06-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b06-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b6b06-125">-Force</span></span>
<span data-ttu-id="b6b06-126">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="b6b06-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b6b06-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6b06-127">-InputObject</span></span>
<span data-ttu-id="b6b06-128">Obiekt centrum wirtualnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="b6b06-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="b6b06-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6b06-129">-Name</span></span>
<span data-ttu-id="b6b06-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b6b06-130">The resource name.</span></span>

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

### <span data-ttu-id="b6b06-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b06-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6b06-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6b06-132">The resource group name.</span></span>

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

### <span data-ttu-id="b6b06-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b06-133">-ResourceId</span></span>
<span data-ttu-id="b6b06-134">Identyfikator zasobu centrum wirtualnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="b6b06-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="b6b06-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6b06-135">-Confirm</span></span>
<span data-ttu-id="b6b06-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b6b06-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b06-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b06-137">-WhatIf</span></span>
<span data-ttu-id="b6b06-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6b06-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b06-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b6b06-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b06-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b06-140">CommonParameters</span></span>
<span data-ttu-id="b6b06-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b06-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b06-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b06-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b06-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6b06-143">INPUTS</span></span>

### <span data-ttu-id="b6b06-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b6b06-144">System.String</span></span>

### <span data-ttu-id="b6b06-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6b06-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b6b06-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6b06-146">OUTPUTS</span></span>

### <span data-ttu-id="b6b06-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6b06-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b6b06-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6b06-148">NOTES</span></span>

## <span data-ttu-id="b6b06-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6b06-149">RELATED LINKS</span></span>

[<span data-ttu-id="b6b06-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b6b06-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
