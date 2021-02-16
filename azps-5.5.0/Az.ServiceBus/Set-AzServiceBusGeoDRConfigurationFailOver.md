---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201578"
---
# <span data-ttu-id="625ad-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="625ad-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="625ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="625ad-102">SYNOPSIS</span></span>
<span data-ttu-id="625ad-103">Wywoływanie trybu failover funkcji DR geolokalizacji i ponowne skonfigurowanie aliasu tak, aby wskazał pomocniczą przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="625ad-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="625ad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="625ad-104">SYNTAX</span></span>

### <span data-ttu-id="625ad-105">GeoDRPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="625ad-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="625ad-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="625ad-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="625ad-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="625ad-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="625ad-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="625ad-108">DESCRIPTION</span></span>
<span data-ttu-id="625ad-109">Polecenie **cmdlet Set-AzServiceBusGeoDRConfigurationFailOver** wywoła failover funkcji DR GEO i ponownie skonfiguruj alias, aby wskazać pomocniczą przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="625ad-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="625ad-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="625ad-110">EXAMPLES</span></span>

### <span data-ttu-id="625ad-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="625ad-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="625ad-112">Wywołuje nazwę trybu failover za pomocą aliasu "SampleDRConfigName", ponownie konfiguruje i wskaż pomocniczą przestrzeń nazw "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="625ad-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="625ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="625ad-113">PARAMETERS</span></span>

### <span data-ttu-id="625ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625ad-114">-DefaultProfile</span></span>
<span data-ttu-id="625ad-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="625ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="625ad-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="625ad-116">-InputObject</span></span>
<span data-ttu-id="625ad-117">Obiekt konfiguracji geodru autobusu usługowego</span><span class="sxs-lookup"><span data-stu-id="625ad-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="625ad-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="625ad-118">-Name</span></span>
<span data-ttu-id="625ad-119">Nazwa konfiguracji dr — alias</span><span class="sxs-lookup"><span data-stu-id="625ad-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="625ad-120">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="625ad-120">-Namespace</span></span>
<span data-ttu-id="625ad-121">Nazwa przestrzeni nazw — pomocnicza przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="625ad-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="625ad-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="625ad-122">-PassThru</span></span>
<span data-ttu-id="625ad-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="625ad-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="625ad-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="625ad-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="625ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="625ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="625ad-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="625ad-126">Resource Group Name</span></span>

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

### <span data-ttu-id="625ad-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="625ad-127">-ResourceId</span></span>
<span data-ttu-id="625ad-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="625ad-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="625ad-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="625ad-129">-Confirm</span></span>
<span data-ttu-id="625ad-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="625ad-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="625ad-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="625ad-131">-WhatIf</span></span>
<span data-ttu-id="625ad-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="625ad-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="625ad-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="625ad-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="625ad-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625ad-134">CommonParameters</span></span>
<span data-ttu-id="625ad-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="625ad-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625ad-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="625ad-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625ad-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="625ad-137">INPUTS</span></span>

### <span data-ttu-id="625ad-138">System.String</span><span class="sxs-lookup"><span data-stu-id="625ad-138">System.String</span></span>

### <span data-ttu-id="625ad-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="625ad-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="625ad-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="625ad-140">OUTPUTS</span></span>

### <span data-ttu-id="625ad-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="625ad-141">System.Boolean</span></span>

## <span data-ttu-id="625ad-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="625ad-142">NOTES</span></span>

## <span data-ttu-id="625ad-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="625ad-143">RELATED LINKS</span></span>
