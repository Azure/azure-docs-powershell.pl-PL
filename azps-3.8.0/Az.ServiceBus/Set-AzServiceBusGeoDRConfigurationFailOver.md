---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050056"
---
# <span data-ttu-id="f9593-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="f9593-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="f9593-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9593-102">SYNOPSIS</span></span>
<span data-ttu-id="f9593-103">Wywołuje tryb failover w trybie GEO DR i ponownie skonfiguruje alias tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="f9593-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="f9593-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9593-104">SYNTAX</span></span>

### <span data-ttu-id="f9593-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f9593-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9593-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f9593-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9593-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9593-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9593-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f9593-108">DESCRIPTION</span></span>
<span data-ttu-id="f9593-109">Polecenie cmdlet **Set-AzServiceBusGeoDRConfigurationFailOver** umożliwia przełączenie do trybu failover w trybie Geo i ponowne skonfigurowanie aliasu tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="f9593-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="f9593-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9593-110">EXAMPLES</span></span>

### <span data-ttu-id="f9593-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9593-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="f9593-112">Wywołuje tryb failover na aliasie "SampleDRConfigName", ponownie konfiguruje i wskazuje pomocniczy obszar nazw "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="f9593-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="f9593-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9593-113">PARAMETERS</span></span>

### <span data-ttu-id="f9593-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9593-114">-DefaultProfile</span></span>
<span data-ttu-id="f9593-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9593-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9593-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9593-116">-InputObject</span></span>
<span data-ttu-id="f9593-117">Obiekt konfiguracji usługi GeoDR Service Bus</span><span class="sxs-lookup"><span data-stu-id="f9593-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="f9593-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9593-118">-Name</span></span>
<span data-ttu-id="f9593-119">Nazwa konfiguracji DR — alias</span><span class="sxs-lookup"><span data-stu-id="f9593-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="f9593-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f9593-120">-Namespace</span></span>
<span data-ttu-id="f9593-121">Nazwa przestrzeni nazw — pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="f9593-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="f9593-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9593-122">-PassThru</span></span>
<span data-ttu-id="f9593-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f9593-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f9593-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f9593-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f9593-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9593-125">-ResourceGroupName</span></span>
<span data-ttu-id="f9593-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f9593-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9593-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9593-127">-ResourceId</span></span>
<span data-ttu-id="f9593-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9593-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="f9593-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9593-129">-Confirm</span></span>
<span data-ttu-id="f9593-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9593-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9593-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9593-131">-WhatIf</span></span>
<span data-ttu-id="f9593-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9593-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9593-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9593-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9593-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9593-134">CommonParameters</span></span>
<span data-ttu-id="f9593-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9593-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9593-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9593-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9593-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9593-137">INPUTS</span></span>

### <span data-ttu-id="f9593-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f9593-138">System.String</span></span>

### <span data-ttu-id="f9593-139">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f9593-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f9593-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9593-140">OUTPUTS</span></span>

### <span data-ttu-id="f9593-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9593-141">System.Boolean</span></span>

## <span data-ttu-id="f9593-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9593-142">NOTES</span></span>

## <span data-ttu-id="f9593-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9593-143">RELATED LINKS</span></span>
