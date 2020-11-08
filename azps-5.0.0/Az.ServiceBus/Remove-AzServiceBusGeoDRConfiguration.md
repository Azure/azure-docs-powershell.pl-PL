---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225506"
---
# <span data-ttu-id="eba99-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="eba99-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="eba99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eba99-102">SYNOPSIS</span></span>
<span data-ttu-id="eba99-103">Usuwanie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="eba99-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="eba99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eba99-104">SYNTAX</span></span>

### <span data-ttu-id="eba99-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eba99-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eba99-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="eba99-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eba99-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eba99-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eba99-108">Opis</span><span class="sxs-lookup"><span data-stu-id="eba99-108">DESCRIPTION</span></span>
<span data-ttu-id="eba99-109">Polecenie cmdlet **Remove-AzServiceBusGeoDRConfiguration** umożliwia usunięcie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="eba99-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="eba99-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eba99-110">EXAMPLES</span></span>

### <span data-ttu-id="eba99-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eba99-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="eba99-112">Usuwanie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="eba99-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="eba99-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eba99-113">PARAMETERS</span></span>

### <span data-ttu-id="eba99-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eba99-114">-AsJob</span></span>
<span data-ttu-id="eba99-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="eba99-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eba99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba99-116">-DefaultProfile</span></span>
<span data-ttu-id="eba99-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eba99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba99-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eba99-118">-InputObject</span></span>
<span data-ttu-id="eba99-119">Obiekt konfiguracji usługi GeoDR Service Bus</span><span class="sxs-lookup"><span data-stu-id="eba99-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="eba99-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eba99-120">-Name</span></span>
<span data-ttu-id="eba99-121">Nazwa aliasu (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="eba99-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="eba99-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eba99-122">-Namespace</span></span>
<span data-ttu-id="eba99-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="eba99-123">Namespace Name</span></span>

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

### <span data-ttu-id="eba99-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eba99-124">-PassThru</span></span>
<span data-ttu-id="eba99-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="eba99-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eba99-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="eba99-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eba99-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba99-127">-ResourceGroupName</span></span>
<span data-ttu-id="eba99-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="eba99-128">Resource Group Name</span></span>

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

### <span data-ttu-id="eba99-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eba99-129">-ResourceId</span></span>
<span data-ttu-id="eba99-130">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="eba99-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="eba99-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eba99-131">-Confirm</span></span>
<span data-ttu-id="eba99-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba99-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba99-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba99-133">-WhatIf</span></span>
<span data-ttu-id="eba99-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba99-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba99-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eba99-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba99-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba99-136">CommonParameters</span></span>
<span data-ttu-id="eba99-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba99-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba99-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eba99-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba99-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eba99-139">INPUTS</span></span>

### <span data-ttu-id="eba99-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eba99-140">System.String</span></span>

### <span data-ttu-id="eba99-141">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="eba99-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="eba99-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eba99-142">OUTPUTS</span></span>

### <span data-ttu-id="eba99-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eba99-143">System.Boolean</span></span>

## <span data-ttu-id="eba99-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eba99-144">NOTES</span></span>

## <span data-ttu-id="eba99-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eba99-145">RELATED LINKS</span></span>
