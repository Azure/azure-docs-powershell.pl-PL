---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c6e711b31dceaf040065750195ce6990b027676b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708154"
---
# <span data-ttu-id="11ede-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="11ede-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="11ede-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11ede-102">SYNOPSIS</span></span>
<span data-ttu-id="11ede-103">Tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="11ede-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="11ede-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11ede-104">SYNTAX</span></span>

### <span data-ttu-id="11ede-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11ede-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ede-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11ede-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ede-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11ede-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11ede-108">Opis</span><span class="sxs-lookup"><span data-stu-id="11ede-108">DESCRIPTION</span></span>
<span data-ttu-id="11ede-109">Polecenie cmdlet **New-AzServiceBusGeoDRConfiguration** tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="11ede-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="11ede-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11ede-110">EXAMPLES</span></span>

### <span data-ttu-id="11ede-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11ede-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="11ede-112">Tworzy alias "SampleDRCongifName" z podstawowym obszarem nazw "SampleNamespace_Primary" z pomocniczym obszarem nazw "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="11ede-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="11ede-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11ede-113">PARAMETERS</span></span>

### <span data-ttu-id="11ede-114">-Symbol alternatywny</span><span class="sxs-lookup"><span data-stu-id="11ede-114">-AlternateName</span></span>
<span data-ttu-id="11ede-115">Symbol zastępczy</span><span class="sxs-lookup"><span data-stu-id="11ede-115">AlternateName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ede-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11ede-116">-AsJob</span></span>
<span data-ttu-id="11ede-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="11ede-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11ede-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ede-118">-DefaultProfile</span></span>
<span data-ttu-id="11ede-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11ede-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ede-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="11ede-120">-InputObject</span></span>
<span data-ttu-id="11ede-121">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="11ede-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11ede-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11ede-122">-Name</span></span>
<span data-ttu-id="11ede-123">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="11ede-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ede-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="11ede-124">-Namespace</span></span>
<span data-ttu-id="11ede-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="11ede-125">Namespace Name</span></span>

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

### <span data-ttu-id="11ede-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="11ede-126">-PartnerNamespace</span></span>
<span data-ttu-id="11ede-127">DR Configuration PartnerNamespace (identyfikator ARM PartnerNamespace [pomocnicza przestrzeń nazw])</span><span class="sxs-lookup"><span data-stu-id="11ede-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ede-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ede-128">-ResourceGroupName</span></span>
<span data-ttu-id="11ede-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="11ede-129">Resource Group Name</span></span>

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

### <span data-ttu-id="11ede-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11ede-130">-ResourceId</span></span>
<span data-ttu-id="11ede-131">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="11ede-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ede-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11ede-132">-Confirm</span></span>
<span data-ttu-id="11ede-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ede-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ede-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ede-134">-WhatIf</span></span>
<span data-ttu-id="11ede-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ede-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ede-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11ede-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ede-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ede-137">CommonParameters</span></span>
<span data-ttu-id="11ede-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ede-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ede-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ede-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ede-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11ede-140">INPUTS</span></span>

### <span data-ttu-id="11ede-141">System. String</span><span class="sxs-lookup"><span data-stu-id="11ede-141">System.String</span></span>

### <span data-ttu-id="11ede-142">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="11ede-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="11ede-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11ede-143">OUTPUTS</span></span>

### <span data-ttu-id="11ede-144">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="11ede-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="11ede-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11ede-145">NOTES</span></span>

## <span data-ttu-id="11ede-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11ede-146">RELATED LINKS</span></span>
