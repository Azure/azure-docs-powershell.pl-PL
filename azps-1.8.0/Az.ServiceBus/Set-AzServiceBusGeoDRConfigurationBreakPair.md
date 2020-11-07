---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 551cf0b883c2af2517240c31a3e633298087534b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708115"
---
# <span data-ttu-id="60db8-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="60db8-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="60db8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60db8-102">SYNOPSIS</span></span>
<span data-ttu-id="60db8-103">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="60db8-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="60db8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60db8-104">SYNTAX</span></span>

### <span data-ttu-id="60db8-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60db8-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60db8-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="60db8-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60db8-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60db8-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60db8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="60db8-108">DESCRIPTION</span></span>
<span data-ttu-id="60db8-109">Polecenie cmdlet **Set-AzServiceBusGeoDRConfigurationBreakPair** wyłącza odzyskiwanie po awarii i zatrzymuje Replikowanie zmian z podstawowych do pomocniczych obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="60db8-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="60db8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60db8-110">EXAMPLES</span></span>

### <span data-ttu-id="60db8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60db8-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="60db8-112">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="60db8-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="60db8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60db8-113">PARAMETERS</span></span>

### <span data-ttu-id="60db8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60db8-114">-DefaultProfile</span></span>
<span data-ttu-id="60db8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60db8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60db8-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="60db8-116">-InputObject</span></span>
<span data-ttu-id="60db8-117">Obiekt konfiguracji usługi GeoDR Service Bus</span><span class="sxs-lookup"><span data-stu-id="60db8-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="60db8-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60db8-118">-Name</span></span>
<span data-ttu-id="60db8-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="60db8-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="60db8-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="60db8-120">-Namespace</span></span>
<span data-ttu-id="60db8-121">Nazwa obszaru nazw — podstawowy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="60db8-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="60db8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60db8-122">-PassThru</span></span>
<span data-ttu-id="60db8-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="60db8-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="60db8-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="60db8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="60db8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60db8-125">-ResourceGroupName</span></span>
<span data-ttu-id="60db8-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="60db8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="60db8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60db8-127">-ResourceId</span></span>
<span data-ttu-id="60db8-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="60db8-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="60db8-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60db8-129">-Confirm</span></span>
<span data-ttu-id="60db8-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60db8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60db8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60db8-131">-WhatIf</span></span>
<span data-ttu-id="60db8-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60db8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60db8-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60db8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60db8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60db8-134">CommonParameters</span></span>
<span data-ttu-id="60db8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60db8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60db8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60db8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60db8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60db8-137">INPUTS</span></span>

### <span data-ttu-id="60db8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="60db8-138">System.String</span></span>

### <span data-ttu-id="60db8-139">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="60db8-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="60db8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60db8-140">OUTPUTS</span></span>

### <span data-ttu-id="60db8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60db8-141">System.Boolean</span></span>

## <span data-ttu-id="60db8-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60db8-142">NOTES</span></span>

## <span data-ttu-id="60db8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60db8-143">RELATED LINKS</span></span>
