---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 581f3c24c8c195b1cafc4962d1c6319418cc07f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543427"
---
# <span data-ttu-id="ab6cb-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab6cb-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="ab6cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab6cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6cb-103">Usuwanie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="ab6cb-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab6cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab6cb-104">SYNTAX</span></span>

### <span data-ttu-id="ab6cb-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ab6cb-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab6cb-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab6cb-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab6cb-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab6cb-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab6cb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ab6cb-108">DESCRIPTION</span></span>
<span data-ttu-id="ab6cb-109">Polecenie cmdlet **Remove-AzureRmServiceBusGeoDRConfiguration** umożliwia usunięcie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="ab6cb-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ab6cb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab6cb-110">EXAMPLES</span></span>

### <span data-ttu-id="ab6cb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab6cb-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="ab6cb-112">Usuwanie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="ab6cb-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ab6cb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab6cb-113">PARAMETERS</span></span>

### <span data-ttu-id="ab6cb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab6cb-114">-AsJob</span></span>
<span data-ttu-id="ab6cb-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ab6cb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab6cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6cb-116">-DefaultProfile</span></span>
<span data-ttu-id="ab6cb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab6cb-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab6cb-118">-InputObject</span></span>
<span data-ttu-id="ab6cb-119">Obiekt konfiguracji usługi GeoDR Service Bus</span><span class="sxs-lookup"><span data-stu-id="ab6cb-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="ab6cb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab6cb-120">-Name</span></span>
<span data-ttu-id="ab6cb-121">Nazwa aliasu (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="ab6cb-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="ab6cb-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ab6cb-122">-Namespace</span></span>
<span data-ttu-id="ab6cb-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="ab6cb-123">Namespace Name</span></span>

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

### <span data-ttu-id="ab6cb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab6cb-124">-PassThru</span></span>
<span data-ttu-id="ab6cb-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ab6cb-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ab6cb-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ab6cb-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ab6cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab6cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab6cb-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ab6cb-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ab6cb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab6cb-129">-ResourceId</span></span>
<span data-ttu-id="ab6cb-130">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab6cb-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="ab6cb-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab6cb-131">-Confirm</span></span>
<span data-ttu-id="ab6cb-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab6cb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab6cb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab6cb-133">-WhatIf</span></span>
<span data-ttu-id="ab6cb-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab6cb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab6cb-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab6cb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab6cb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6cb-136">CommonParameters</span></span>
<span data-ttu-id="ab6cb-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab6cb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6cb-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab6cb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6cb-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab6cb-139">INPUTS</span></span>

### <span data-ttu-id="ab6cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ab6cb-140">System.String</span></span>

### <span data-ttu-id="ab6cb-141">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ab6cb-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="ab6cb-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab6cb-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ab6cb-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab6cb-143">OUTPUTS</span></span>

### <span data-ttu-id="ab6cb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab6cb-144">System.Boolean</span></span>

## <span data-ttu-id="ab6cb-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab6cb-145">NOTES</span></span>

## <span data-ttu-id="ab6cb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab6cb-146">RELATED LINKS</span></span>
