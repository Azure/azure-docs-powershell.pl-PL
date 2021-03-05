---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: b75eb7e9bbac3efddc49bcccf384f288c01960a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996220"
---
# <span data-ttu-id="fd8ec-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="fd8ec-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="fd8ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8ec-103">Usuń zasób urządzenia wirtualnego sieci.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="fd8ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd8ec-104">SYNTAX</span></span>

### <span data-ttu-id="fd8ec-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fd8ec-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd8ec-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd8ec-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd8ec-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd8ec-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd8ec-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd8ec-108">DESCRIPTION</span></span>
<span data-ttu-id="fd8ec-109">Polecenie Remove-AzNetworkVirtualAppliance usuwa zasób wirtualnego urządzenia sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="fd8ec-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd8ec-110">EXAMPLES</span></span>

### <span data-ttu-id="fd8ec-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd8ec-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="fd8ec-112">Usuwanie zasobu urządzenia wirtualnego sieci.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="fd8ec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd8ec-113">PARAMETERS</span></span>

### <span data-ttu-id="fd8ec-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fd8ec-114">-AsJob</span></span>
<span data-ttu-id="fd8ec-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fd8ec-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd8ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8ec-116">-DefaultProfile</span></span>
<span data-ttu-id="fd8ec-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd8ec-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fd8ec-118">-Force</span></span>
<span data-ttu-id="fd8ec-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fd8ec-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fd8ec-120">-Name</span></span>
<span data-ttu-id="fd8ec-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8ec-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="fd8ec-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="fd8ec-123">Obiekt zasobu.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8ec-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd8ec-124">-PassThru</span></span>
<span data-ttu-id="fd8ec-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fd8ec-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd8ec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd8ec-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd8ec-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8ec-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd8ec-129">-ResourceId</span></span>
<span data-ttu-id="fd8ec-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-130">The Resource Id.</span></span>

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

### <span data-ttu-id="fd8ec-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd8ec-131">-Confirm</span></span>
<span data-ttu-id="fd8ec-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd8ec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd8ec-133">-WhatIf</span></span>
<span data-ttu-id="fd8ec-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8ec-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd8ec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8ec-136">CommonParameters</span></span>
<span data-ttu-id="fd8ec-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd8ec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8ec-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd8ec-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8ec-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd8ec-139">INPUTS</span></span>

### <span data-ttu-id="fd8ec-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fd8ec-140">System.String</span></span>

### <span data-ttu-id="fd8ec-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="fd8ec-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="fd8ec-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd8ec-142">OUTPUTS</span></span>

### <span data-ttu-id="fd8ec-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd8ec-143">System.Boolean</span></span>

## <span data-ttu-id="fd8ec-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd8ec-144">NOTES</span></span>

## <span data-ttu-id="fd8ec-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd8ec-145">RELATED LINKS</span></span>
