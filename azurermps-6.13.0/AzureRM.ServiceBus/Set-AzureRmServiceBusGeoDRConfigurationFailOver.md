---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 274563165beefdc8a5d7575bd32328f68bf40efa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551124"
---
# <span data-ttu-id="46a19-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="46a19-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="46a19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46a19-102">SYNOPSIS</span></span>
<span data-ttu-id="46a19-103">Wywołuje tryb failover w trybie GEO DR i ponownie skonfiguruje alias tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="46a19-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46a19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46a19-104">SYNTAX</span></span>

### <span data-ttu-id="46a19-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="46a19-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46a19-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="46a19-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a19-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46a19-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a19-108">Opis</span><span class="sxs-lookup"><span data-stu-id="46a19-108">DESCRIPTION</span></span>
<span data-ttu-id="46a19-109">Polecenie cmdlet **Set-AzureRmServiceBusGeoDRConfigurationFailOver** ENVOKES Geo Dr failover oraz Zmień konfigurację aliasu tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="46a19-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="46a19-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46a19-110">EXAMPLES</span></span>

### <span data-ttu-id="46a19-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46a19-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="46a19-112">Wywołuje tryb failover na aliasie "SampleDRCongifName", ponownie konfiguruje i wskazuje pomocniczy obszar nazw "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="46a19-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="46a19-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46a19-113">PARAMETERS</span></span>

### <span data-ttu-id="46a19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a19-114">-DefaultProfile</span></span>
<span data-ttu-id="46a19-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46a19-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a19-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46a19-116">-InputObject</span></span>
<span data-ttu-id="46a19-117">Obiekt konfiguracji usługi GeoDR Service Bus</span><span class="sxs-lookup"><span data-stu-id="46a19-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="46a19-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46a19-118">-Name</span></span>
<span data-ttu-id="46a19-119">Nazwa konfiguracji DR — alias</span><span class="sxs-lookup"><span data-stu-id="46a19-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="46a19-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="46a19-120">-Namespace</span></span>
<span data-ttu-id="46a19-121">Nazwa przestrzeni nazw — pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="46a19-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="46a19-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46a19-122">-PassThru</span></span>
<span data-ttu-id="46a19-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="46a19-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="46a19-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="46a19-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46a19-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a19-125">-ResourceGroupName</span></span>
<span data-ttu-id="46a19-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="46a19-126">Resource Group Name</span></span>

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

### <span data-ttu-id="46a19-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46a19-127">-ResourceId</span></span>
<span data-ttu-id="46a19-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="46a19-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="46a19-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46a19-129">-Confirm</span></span>
<span data-ttu-id="46a19-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46a19-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a19-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a19-131">-WhatIf</span></span>
<span data-ttu-id="46a19-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46a19-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a19-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46a19-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a19-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a19-134">CommonParameters</span></span>
<span data-ttu-id="46a19-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a19-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a19-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a19-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a19-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46a19-137">INPUTS</span></span>

### <span data-ttu-id="46a19-138">System. String</span><span class="sxs-lookup"><span data-stu-id="46a19-138">System.String</span></span>

### <span data-ttu-id="46a19-139">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="46a19-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="46a19-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46a19-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="46a19-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46a19-141">OUTPUTS</span></span>

### <span data-ttu-id="46a19-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46a19-142">System.Boolean</span></span>

## <span data-ttu-id="46a19-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46a19-143">NOTES</span></span>

## <span data-ttu-id="46a19-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46a19-144">RELATED LINKS</span></span>
