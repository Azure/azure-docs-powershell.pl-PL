---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: da4df1206035e5ecae1a21d70e67091e852b1c51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717306"
---
# <span data-ttu-id="a5c91-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="a5c91-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="a5c91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5c91-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c91-103">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="a5c91-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5c91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5c91-104">SYNTAX</span></span>

### <span data-ttu-id="a5c91-105">GeoDRBreakPairFailOverPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5c91-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c91-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a5c91-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c91-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c91-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c91-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a5c91-108">DESCRIPTION</span></span>
<span data-ttu-id="a5c91-109">Polecenie cmdlet **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** wyłącza odzyskiwanie po awarii i zatrzymuje Replikowanie zmian z podstawowych do pomocniczych obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="a5c91-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="a5c91-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5c91-110">EXAMPLES</span></span>

### <span data-ttu-id="a5c91-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5c91-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="a5c91-112">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="a5c91-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="a5c91-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5c91-113">PARAMETERS</span></span>

### <span data-ttu-id="a5c91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c91-114">-DefaultProfile</span></span>
<span data-ttu-id="a5c91-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5c91-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5c91-116">-InputObject</span></span>
<span data-ttu-id="a5c91-117">Obiekt konfiguracji usługi GeoDR Service Bus</span><span class="sxs-lookup"><span data-stu-id="a5c91-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5c91-118">-Name</span></span>
<span data-ttu-id="a5c91-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="a5c91-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a5c91-120">-Namespace</span></span>
<span data-ttu-id="a5c91-121">Nazwa obszaru nazw — podstawowy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="a5c91-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5c91-122">-PassThru</span></span>
<span data-ttu-id="a5c91-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a5c91-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5c91-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a5c91-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c91-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5c91-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a5c91-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c91-127">-ResourceId</span></span>
<span data-ttu-id="a5c91-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5c91-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5c91-129">-Confirm</span></span>
<span data-ttu-id="a5c91-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5c91-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c91-131">-WhatIf</span></span>
<span data-ttu-id="a5c91-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5c91-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c91-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5c91-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c91-134">CommonParameters</span></span>
<span data-ttu-id="a5c91-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a5c91-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c91-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c91-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5c91-137">INPUTS</span></span>

### <span data-ttu-id="a5c91-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c91-138">System.String</span></span>
<span data-ttu-id="a5c91-139">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a5c91-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="a5c91-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5c91-140">OUTPUTS</span></span>

### <span data-ttu-id="a5c91-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5c91-141">System.Boolean</span></span>


## <span data-ttu-id="a5c91-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5c91-142">NOTES</span></span>

## <span data-ttu-id="a5c91-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5c91-143">RELATED LINKS</span></span>
