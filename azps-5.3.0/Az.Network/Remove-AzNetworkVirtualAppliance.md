---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500230"
---
# <span data-ttu-id="f58b5-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f58b5-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="f58b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f58b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f58b5-103">Usuwanie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="f58b5-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="f58b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f58b5-104">SYNTAX</span></span>

### <span data-ttu-id="f58b5-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f58b5-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f58b5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f58b5-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f58b5-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f58b5-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f58b5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f58b5-108">DESCRIPTION</span></span>
<span data-ttu-id="f58b5-109">Polecenie Remove-AzNetworkVirtualAppliance powoduje usunięcie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="f58b5-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="f58b5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f58b5-110">EXAMPLES</span></span>

### <span data-ttu-id="f58b5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f58b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="f58b5-112">Usuwanie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="f58b5-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="f58b5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f58b5-113">PARAMETERS</span></span>

### <span data-ttu-id="f58b5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f58b5-114">-AsJob</span></span>
<span data-ttu-id="f58b5-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f58b5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f58b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f58b5-116">-DefaultProfile</span></span>
<span data-ttu-id="f58b5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f58b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f58b5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f58b5-118">-Force</span></span>
<span data-ttu-id="f58b5-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f58b5-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f58b5-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f58b5-120">-Name</span></span>
<span data-ttu-id="f58b5-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f58b5-121">The resource name.</span></span>

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

### <span data-ttu-id="f58b5-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f58b5-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="f58b5-123">Obiekt Resource.</span><span class="sxs-lookup"><span data-stu-id="f58b5-123">The resource object.</span></span>

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

### <span data-ttu-id="f58b5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f58b5-124">-PassThru</span></span>
<span data-ttu-id="f58b5-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f58b5-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f58b5-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f58b5-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f58b5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f58b5-127">-ResourceGroupName</span></span>
<span data-ttu-id="f58b5-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f58b5-128">The resource group name.</span></span>

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

### <span data-ttu-id="f58b5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f58b5-129">-ResourceId</span></span>
<span data-ttu-id="f58b5-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f58b5-130">The Resource Id.</span></span>

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

### <span data-ttu-id="f58b5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f58b5-131">-Confirm</span></span>
<span data-ttu-id="f58b5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f58b5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f58b5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f58b5-133">-WhatIf</span></span>
<span data-ttu-id="f58b5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f58b5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f58b5-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f58b5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f58b5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58b5-136">CommonParameters</span></span>
<span data-ttu-id="f58b5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f58b5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58b5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f58b5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58b5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f58b5-139">INPUTS</span></span>

### <span data-ttu-id="f58b5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f58b5-140">System.String</span></span>

### <span data-ttu-id="f58b5-141">Microsoft. Azure. Commands. Network. models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f58b5-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="f58b5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f58b5-142">OUTPUTS</span></span>

### <span data-ttu-id="f58b5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f58b5-143">System.Boolean</span></span>

## <span data-ttu-id="f58b5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f58b5-144">NOTES</span></span>

## <span data-ttu-id="f58b5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f58b5-145">RELATED LINKS</span></span>
