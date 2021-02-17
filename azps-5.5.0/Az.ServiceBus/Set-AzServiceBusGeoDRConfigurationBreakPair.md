---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f45899b1c2d397245461a10a6e2648f92dc9da40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183514"
---
# <span data-ttu-id="ea0d5-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="ea0d5-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="ea0d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea0d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0d5-103">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowej do pomocniczej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="ea0d5-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="ea0d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea0d5-104">SYNTAX</span></span>

### <span data-ttu-id="ea0d5-105">GeoDRPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ea0d5-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea0d5-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ea0d5-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea0d5-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea0d5-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea0d5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea0d5-108">DESCRIPTION</span></span>
<span data-ttu-id="ea0d5-109">Polecenie **cmdlet Set-AzServiceBusGeoDRConfigurationBreakPair** wyłącza odzyskiwanie po awarii i przestaje replikować zmiany z podstawowych do pomocniczych przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="ea0d5-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="ea0d5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea0d5-110">EXAMPLES</span></span>

### <span data-ttu-id="ea0d5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea0d5-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="ea0d5-112">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowej na pomocniczą przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="ea0d5-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="ea0d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea0d5-113">PARAMETERS</span></span>

### <span data-ttu-id="ea0d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0d5-114">-DefaultProfile</span></span>
<span data-ttu-id="ea0d5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0d5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea0d5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea0d5-116">-InputObject</span></span>
<span data-ttu-id="ea0d5-117">Obiekt konfiguracji geodru typu service bus</span><span class="sxs-lookup"><span data-stu-id="ea0d5-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d5-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ea0d5-118">-Name</span></span>
<span data-ttu-id="ea0d5-119">Nazwa konfiguracji dr</span><span class="sxs-lookup"><span data-stu-id="ea0d5-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d5-120">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="ea0d5-120">-Namespace</span></span>
<span data-ttu-id="ea0d5-121">Nazwa przestrzeni nazw — podstawowa przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="ea0d5-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea0d5-122">-PassThru</span></span>
<span data-ttu-id="ea0d5-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ea0d5-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea0d5-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ea0d5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea0d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea0d5-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ea0d5-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea0d5-127">-ResourceId</span></span>
<span data-ttu-id="ea0d5-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea0d5-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d5-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea0d5-129">-Confirm</span></span>
<span data-ttu-id="ea0d5-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea0d5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0d5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0d5-131">-WhatIf</span></span>
<span data-ttu-id="ea0d5-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea0d5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea0d5-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ea0d5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0d5-134">CommonParameters</span></span>
<span data-ttu-id="ea0d5-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0d5-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0d5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0d5-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea0d5-137">INPUTS</span></span>

### <span data-ttu-id="ea0d5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ea0d5-138">System.String</span></span>

### <span data-ttu-id="ea0d5-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ea0d5-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="ea0d5-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea0d5-140">OUTPUTS</span></span>

### <span data-ttu-id="ea0d5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea0d5-141">System.Boolean</span></span>

## <span data-ttu-id="ea0d5-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea0d5-142">NOTES</span></span>

## <span data-ttu-id="ea0d5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea0d5-143">RELATED LINKS</span></span>
