---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 663718c97680e70fc31d8e581ff308444eb4c6c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708113"
---
# <span data-ttu-id="b3d73-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="b3d73-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="b3d73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3d73-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d73-103">Wywołuje tryb failover w trybie GEO DR i ponownie skonfiguruje alias tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="b3d73-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="b3d73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3d73-104">SYNTAX</span></span>

### <span data-ttu-id="b3d73-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3d73-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d73-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b3d73-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d73-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3d73-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3d73-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b3d73-108">DESCRIPTION</span></span>
<span data-ttu-id="b3d73-109">Polecenie cmdlet **Set-AzServiceBusGeoDRConfigurationFailOver** ENVOKES Geo Dr failover oraz Zmień konfigurację aliasu tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="b3d73-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="b3d73-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3d73-110">EXAMPLES</span></span>

### <span data-ttu-id="b3d73-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3d73-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="b3d73-112">Wywołuje tryb failover na aliasie "SampleDRCongifName", ponownie konfiguruje i wskazuje pomocniczy obszar nazw "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="b3d73-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="b3d73-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3d73-113">PARAMETERS</span></span>

### <span data-ttu-id="b3d73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d73-114">-DefaultProfile</span></span>
<span data-ttu-id="b3d73-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3d73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d73-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3d73-116">-InputObject</span></span>
<span data-ttu-id="b3d73-117">Obiekt konfiguracji usługi GeoDR Service Bus</span><span class="sxs-lookup"><span data-stu-id="b3d73-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="b3d73-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3d73-118">-Name</span></span>
<span data-ttu-id="b3d73-119">Nazwa konfiguracji DR — alias</span><span class="sxs-lookup"><span data-stu-id="b3d73-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="b3d73-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b3d73-120">-Namespace</span></span>
<span data-ttu-id="b3d73-121">Nazwa przestrzeni nazw — pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="b3d73-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="b3d73-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3d73-122">-PassThru</span></span>
<span data-ttu-id="b3d73-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b3d73-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3d73-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b3d73-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3d73-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d73-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3d73-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b3d73-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b3d73-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3d73-127">-ResourceId</span></span>
<span data-ttu-id="b3d73-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3d73-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="b3d73-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3d73-129">-Confirm</span></span>
<span data-ttu-id="b3d73-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3d73-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3d73-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3d73-131">-WhatIf</span></span>
<span data-ttu-id="b3d73-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3d73-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3d73-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3d73-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3d73-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d73-134">CommonParameters</span></span>
<span data-ttu-id="b3d73-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d73-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d73-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3d73-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d73-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3d73-137">INPUTS</span></span>

### <span data-ttu-id="b3d73-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d73-138">System.String</span></span>

### <span data-ttu-id="b3d73-139">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b3d73-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="b3d73-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3d73-140">OUTPUTS</span></span>

### <span data-ttu-id="b3d73-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3d73-141">System.Boolean</span></span>

## <span data-ttu-id="b3d73-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3d73-142">NOTES</span></span>

## <span data-ttu-id="b3d73-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3d73-143">RELATED LINKS</span></span>
