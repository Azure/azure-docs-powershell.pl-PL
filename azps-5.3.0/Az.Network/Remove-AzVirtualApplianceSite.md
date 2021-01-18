---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501211"
---
# <span data-ttu-id="a71c6-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a71c6-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="a71c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a71c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a71c6-103">Usuwanie witryny urządzenia wirtualnego z sieciowego zasobu urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a71c6-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a71c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a71c6-104">SYNTAX</span></span>

### <span data-ttu-id="a71c6-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a71c6-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a71c6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a71c6-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a71c6-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a71c6-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71c6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a71c6-108">DESCRIPTION</span></span>
<span data-ttu-id="a71c6-109">Polecenie Remove-AzVirtualApplianceSite usuwa witrynę urządzenia wirtualnego z sieciowego zasobu urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a71c6-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a71c6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a71c6-110">EXAMPLES</span></span>

### <span data-ttu-id="a71c6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a71c6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="a71c6-112">Usuwanie zasobu witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a71c6-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="a71c6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a71c6-113">PARAMETERS</span></span>

### <span data-ttu-id="a71c6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a71c6-114">-AsJob</span></span>
<span data-ttu-id="a71c6-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a71c6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a71c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71c6-116">-DefaultProfile</span></span>
<span data-ttu-id="a71c6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a71c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a71c6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a71c6-118">-Force</span></span>
<span data-ttu-id="a71c6-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a71c6-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a71c6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a71c6-120">-Name</span></span>
<span data-ttu-id="a71c6-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a71c6-121">The resource name.</span></span>

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

### <span data-ttu-id="a71c6-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="a71c6-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="a71c6-123">Identyfikator zasobu wirtualnego urządzenia sieciowego skojarzonego z tą witryną.</span><span class="sxs-lookup"><span data-stu-id="a71c6-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="a71c6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a71c6-124">-PassThru</span></span>
<span data-ttu-id="a71c6-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a71c6-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a71c6-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a71c6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a71c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a71c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="a71c6-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a71c6-128">The resource group name.</span></span>

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

### <span data-ttu-id="a71c6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a71c6-129">-ResourceId</span></span>
<span data-ttu-id="a71c6-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a71c6-130">The resource id.</span></span>

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

### <span data-ttu-id="a71c6-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a71c6-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="a71c6-132">Obiekt witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a71c6-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="a71c6-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a71c6-133">-Confirm</span></span>
<span data-ttu-id="a71c6-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71c6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a71c6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71c6-135">-WhatIf</span></span>
<span data-ttu-id="a71c6-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71c6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a71c6-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a71c6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a71c6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71c6-138">CommonParameters</span></span>
<span data-ttu-id="a71c6-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a71c6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71c6-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a71c6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71c6-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a71c6-141">INPUTS</span></span>

### <span data-ttu-id="a71c6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a71c6-142">System.String</span></span>

### <span data-ttu-id="a71c6-143">Microsoft. Azure. Commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a71c6-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="a71c6-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a71c6-144">OUTPUTS</span></span>

### <span data-ttu-id="a71c6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a71c6-145">System.Boolean</span></span>

## <span data-ttu-id="a71c6-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a71c6-146">NOTES</span></span>

## <span data-ttu-id="a71c6-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a71c6-147">RELATED LINKS</span></span>
