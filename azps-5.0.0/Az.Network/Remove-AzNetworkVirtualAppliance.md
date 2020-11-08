---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225850"
---
# <span data-ttu-id="d3211-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d3211-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="d3211-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3211-102">SYNOPSIS</span></span>
<span data-ttu-id="d3211-103">Usuwanie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="d3211-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d3211-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3211-104">SYNTAX</span></span>

### <span data-ttu-id="d3211-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d3211-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3211-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3211-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3211-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3211-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3211-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d3211-108">DESCRIPTION</span></span>
<span data-ttu-id="d3211-109">Polecenie Remove-AzNetworkVirtualAppliance powoduje usunięcie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="d3211-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d3211-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3211-110">EXAMPLES</span></span>

### <span data-ttu-id="d3211-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3211-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="d3211-112">Usuwanie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="d3211-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d3211-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3211-113">PARAMETERS</span></span>

### <span data-ttu-id="d3211-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3211-114">-AsJob</span></span>
<span data-ttu-id="d3211-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d3211-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3211-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3211-116">-DefaultProfile</span></span>
<span data-ttu-id="d3211-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3211-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3211-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d3211-118">-Force</span></span>
<span data-ttu-id="d3211-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3211-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d3211-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d3211-120">-Name</span></span>
<span data-ttu-id="d3211-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d3211-121">The resource name.</span></span>

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

### <span data-ttu-id="d3211-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d3211-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="d3211-123">Obiekt Resource.</span><span class="sxs-lookup"><span data-stu-id="d3211-123">The resource object.</span></span>

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

### <span data-ttu-id="d3211-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3211-124">-PassThru</span></span>
<span data-ttu-id="d3211-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d3211-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d3211-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d3211-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3211-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3211-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3211-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3211-128">The resource group name.</span></span>

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

### <span data-ttu-id="d3211-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3211-129">-ResourceId</span></span>
<span data-ttu-id="d3211-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d3211-130">The Resource Id.</span></span>

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

### <span data-ttu-id="d3211-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3211-131">-Confirm</span></span>
<span data-ttu-id="d3211-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3211-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3211-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3211-133">-WhatIf</span></span>
<span data-ttu-id="d3211-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3211-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3211-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3211-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3211-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3211-136">CommonParameters</span></span>
<span data-ttu-id="d3211-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3211-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3211-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3211-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3211-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3211-139">INPUTS</span></span>

### <span data-ttu-id="d3211-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d3211-140">System.String</span></span>

### <span data-ttu-id="d3211-141">Microsoft. Azure. Commands. Network. models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d3211-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="d3211-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3211-142">OUTPUTS</span></span>

### <span data-ttu-id="d3211-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3211-143">System.Boolean</span></span>

## <span data-ttu-id="d3211-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3211-144">NOTES</span></span>

## <span data-ttu-id="d3211-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3211-145">RELATED LINKS</span></span>
