---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352990"
---
# <span data-ttu-id="b8b2e-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b8b2e-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="b8b2e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b2e-103">Usuwanie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b8b2e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8b2e-104">SYNTAX</span></span>

### <span data-ttu-id="b8b2e-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b8b2e-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b2e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8b2e-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b2e-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8b2e-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8b2e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b8b2e-108">DESCRIPTION</span></span>
<span data-ttu-id="b8b2e-109">Polecenie Remove-AzNetworkVirtualAppliance powoduje usunięcie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b8b2e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8b2e-110">EXAMPLES</span></span>

### <span data-ttu-id="b8b2e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8b2e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="b8b2e-112">Usuwanie zasobu sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b8b2e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8b2e-113">PARAMETERS</span></span>

### <span data-ttu-id="b8b2e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8b2e-114">-AsJob</span></span>
<span data-ttu-id="b8b2e-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b8b2e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8b2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b2e-116">-DefaultProfile</span></span>
<span data-ttu-id="b8b2e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8b2e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b8b2e-118">-Force</span></span>
<span data-ttu-id="b8b2e-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b8b2e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8b2e-120">-Name</span></span>
<span data-ttu-id="b8b2e-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-121">The resource name.</span></span>

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

### <span data-ttu-id="b8b2e-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b8b2e-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="b8b2e-123">Obiekt Resource.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-123">The resource object.</span></span>

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

### <span data-ttu-id="b8b2e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8b2e-124">-PassThru</span></span>
<span data-ttu-id="b8b2e-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b8b2e-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b8b2e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8b2e-127">-ResourceGroupName</span></span>
<span data-ttu-id="b8b2e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-128">The resource group name.</span></span>

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

### <span data-ttu-id="b8b2e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8b2e-129">-ResourceId</span></span>
<span data-ttu-id="b8b2e-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-130">The Resource Id.</span></span>

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

### <span data-ttu-id="b8b2e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8b2e-131">-Confirm</span></span>
<span data-ttu-id="b8b2e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8b2e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8b2e-133">-WhatIf</span></span>
<span data-ttu-id="b8b2e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8b2e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8b2e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b2e-136">CommonParameters</span></span>
<span data-ttu-id="b8b2e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b2e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8b2e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b2e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8b2e-139">INPUTS</span></span>

### <span data-ttu-id="b8b2e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b8b2e-140">System.String</span></span>

### <span data-ttu-id="b8b2e-141">Microsoft. Azure. Commands. Network. models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b8b2e-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="b8b2e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8b2e-142">OUTPUTS</span></span>

### <span data-ttu-id="b8b2e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8b2e-143">System.Boolean</span></span>

## <span data-ttu-id="b8b2e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8b2e-144">NOTES</span></span>

## <span data-ttu-id="b8b2e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8b2e-145">RELATED LINKS</span></span>
