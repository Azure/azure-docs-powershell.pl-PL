---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202505"
---
# <span data-ttu-id="5a57a-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5a57a-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="5a57a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a57a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a57a-103">Usuwanie witryny urządzenia wirtualnego z zasobu Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="5a57a-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5a57a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a57a-104">SYNTAX</span></span>

### <span data-ttu-id="5a57a-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5a57a-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a57a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a57a-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a57a-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a57a-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a57a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a57a-108">DESCRIPTION</span></span>
<span data-ttu-id="5a57a-109">Polecenie Remove-AzVirtualApplianceSite usuwa witrynę wirtualnego urządzenia z zasobu Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="5a57a-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5a57a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a57a-110">EXAMPLES</span></span>

### <span data-ttu-id="5a57a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a57a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="5a57a-112">Usuń zasób witryny Urządzenie wirtualne.</span><span class="sxs-lookup"><span data-stu-id="5a57a-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="5a57a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a57a-113">PARAMETERS</span></span>

### <span data-ttu-id="5a57a-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5a57a-114">-AsJob</span></span>
<span data-ttu-id="5a57a-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5a57a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a57a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a57a-116">-DefaultProfile</span></span>
<span data-ttu-id="5a57a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a57a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a57a-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5a57a-118">-Force</span></span>
<span data-ttu-id="5a57a-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a57a-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5a57a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a57a-120">-Name</span></span>
<span data-ttu-id="5a57a-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5a57a-121">The resource name.</span></span>

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

### <span data-ttu-id="5a57a-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="5a57a-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="5a57a-123">Identyfikator zasobu wirtualnego urządzenia sieciowego skojarzonego z tą witryną.</span><span class="sxs-lookup"><span data-stu-id="5a57a-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="5a57a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a57a-124">-PassThru</span></span>
<span data-ttu-id="5a57a-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5a57a-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="5a57a-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5a57a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a57a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a57a-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a57a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a57a-128">The resource group name.</span></span>

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

### <span data-ttu-id="5a57a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a57a-129">-ResourceId</span></span>
<span data-ttu-id="5a57a-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5a57a-130">The resource id.</span></span>

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

### <span data-ttu-id="5a57a-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5a57a-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="5a57a-132">Obiekt witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="5a57a-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="5a57a-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a57a-133">-Confirm</span></span>
<span data-ttu-id="5a57a-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a57a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a57a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a57a-135">-WhatIf</span></span>
<span data-ttu-id="5a57a-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a57a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a57a-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a57a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a57a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a57a-138">CommonParameters</span></span>
<span data-ttu-id="5a57a-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a57a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a57a-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a57a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a57a-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a57a-141">INPUTS</span></span>

### <span data-ttu-id="5a57a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5a57a-142">System.String</span></span>

### <span data-ttu-id="5a57a-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5a57a-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="5a57a-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a57a-144">OUTPUTS</span></span>

### <span data-ttu-id="5a57a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a57a-145">System.Boolean</span></span>

## <span data-ttu-id="5a57a-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a57a-146">NOTES</span></span>

## <span data-ttu-id="5a57a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a57a-147">RELATED LINKS</span></span>
