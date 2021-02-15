---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186946"
---
# <span data-ttu-id="48349-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="48349-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="48349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48349-102">SYNOPSIS</span></span>
<span data-ttu-id="48349-103">Usuń zasób urządzenia wirtualnego sieci.</span><span class="sxs-lookup"><span data-stu-id="48349-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="48349-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48349-104">SYNTAX</span></span>

### <span data-ttu-id="48349-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="48349-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48349-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48349-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48349-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48349-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48349-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="48349-108">DESCRIPTION</span></span>
<span data-ttu-id="48349-109">Polecenie Remove-AzNetworkVirtualAppliance usuwa zasób wirtualnego urządzenia sieciowego.</span><span class="sxs-lookup"><span data-stu-id="48349-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="48349-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48349-110">EXAMPLES</span></span>

### <span data-ttu-id="48349-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48349-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="48349-112">Usuwanie zasobu urządzenia wirtualnego sieci.</span><span class="sxs-lookup"><span data-stu-id="48349-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="48349-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48349-113">PARAMETERS</span></span>

### <span data-ttu-id="48349-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="48349-114">-AsJob</span></span>
<span data-ttu-id="48349-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="48349-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48349-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48349-116">-DefaultProfile</span></span>
<span data-ttu-id="48349-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48349-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48349-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="48349-118">-Force</span></span>
<span data-ttu-id="48349-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48349-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="48349-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="48349-120">-Name</span></span>
<span data-ttu-id="48349-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="48349-121">The resource name.</span></span>

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

### <span data-ttu-id="48349-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="48349-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="48349-123">Obiekt zasobu.</span><span class="sxs-lookup"><span data-stu-id="48349-123">The resource object.</span></span>

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

### <span data-ttu-id="48349-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48349-124">-PassThru</span></span>
<span data-ttu-id="48349-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="48349-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="48349-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="48349-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48349-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48349-127">-ResourceGroupName</span></span>
<span data-ttu-id="48349-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48349-128">The resource group name.</span></span>

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

### <span data-ttu-id="48349-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48349-129">-ResourceId</span></span>
<span data-ttu-id="48349-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="48349-130">The Resource Id.</span></span>

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

### <span data-ttu-id="48349-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48349-131">-Confirm</span></span>
<span data-ttu-id="48349-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48349-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48349-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48349-133">-WhatIf</span></span>
<span data-ttu-id="48349-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48349-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48349-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="48349-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48349-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48349-136">CommonParameters</span></span>
<span data-ttu-id="48349-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48349-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48349-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48349-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48349-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48349-139">INPUTS</span></span>

### <span data-ttu-id="48349-140">System.String</span><span class="sxs-lookup"><span data-stu-id="48349-140">System.String</span></span>

### <span data-ttu-id="48349-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="48349-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="48349-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48349-142">OUTPUTS</span></span>

### <span data-ttu-id="48349-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48349-143">System.Boolean</span></span>

## <span data-ttu-id="48349-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48349-144">NOTES</span></span>

## <span data-ttu-id="48349-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48349-145">RELATED LINKS</span></span>
