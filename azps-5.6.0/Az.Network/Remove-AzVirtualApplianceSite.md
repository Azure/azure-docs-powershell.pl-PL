---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 1456acb101302297e807d6d46bf83183e8a6e523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006122"
---
# <span data-ttu-id="34944-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="34944-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="34944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34944-102">SYNOPSIS</span></span>
<span data-ttu-id="34944-103">Usuwanie witryny urządzenia wirtualnego z zasobu Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="34944-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="34944-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34944-104">SYNTAX</span></span>

### <span data-ttu-id="34944-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="34944-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34944-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34944-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34944-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34944-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34944-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="34944-108">DESCRIPTION</span></span>
<span data-ttu-id="34944-109">Polecenie Remove-AzVirtualApplianceSite usuwa witrynę wirtualnego urządzenia z zasobu Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="34944-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="34944-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34944-110">EXAMPLES</span></span>

### <span data-ttu-id="34944-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34944-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="34944-112">Usuń zasób witryny Urządzenie wirtualne.</span><span class="sxs-lookup"><span data-stu-id="34944-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="34944-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34944-113">PARAMETERS</span></span>

### <span data-ttu-id="34944-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="34944-114">-AsJob</span></span>
<span data-ttu-id="34944-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="34944-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34944-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34944-116">-DefaultProfile</span></span>
<span data-ttu-id="34944-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34944-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34944-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="34944-118">-Force</span></span>
<span data-ttu-id="34944-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34944-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="34944-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34944-120">-Name</span></span>
<span data-ttu-id="34944-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="34944-121">The resource name.</span></span>

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

### <span data-ttu-id="34944-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="34944-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="34944-123">Identyfikator zasobu wirtualnego urządzenia sieciowego skojarzonego z tą witryną.</span><span class="sxs-lookup"><span data-stu-id="34944-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="34944-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34944-124">-PassThru</span></span>
<span data-ttu-id="34944-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="34944-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="34944-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="34944-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34944-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34944-127">-ResourceGroupName</span></span>
<span data-ttu-id="34944-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34944-128">The resource group name.</span></span>

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

### <span data-ttu-id="34944-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34944-129">-ResourceId</span></span>
<span data-ttu-id="34944-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="34944-130">The resource id.</span></span>

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

### <span data-ttu-id="34944-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="34944-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="34944-132">Obiekt witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="34944-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34944-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34944-133">-Confirm</span></span>
<span data-ttu-id="34944-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34944-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34944-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34944-135">-WhatIf</span></span>
<span data-ttu-id="34944-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34944-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34944-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="34944-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34944-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34944-138">CommonParameters</span></span>
<span data-ttu-id="34944-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34944-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34944-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34944-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34944-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34944-141">INPUTS</span></span>

### <span data-ttu-id="34944-142">System.String</span><span class="sxs-lookup"><span data-stu-id="34944-142">System.String</span></span>

### <span data-ttu-id="34944-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="34944-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="34944-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34944-144">OUTPUTS</span></span>

### <span data-ttu-id="34944-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34944-145">System.Boolean</span></span>

## <span data-ttu-id="34944-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34944-146">NOTES</span></span>

## <span data-ttu-id="34944-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34944-147">RELATED LINKS</span></span>
