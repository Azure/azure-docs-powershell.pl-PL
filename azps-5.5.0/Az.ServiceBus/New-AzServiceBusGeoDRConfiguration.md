---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197866"
---
# <span data-ttu-id="cdfa9-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdfa9-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="cdfa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfa9-103">Tworzy nowy alias(konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="cdfa9-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="cdfa9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cdfa9-104">SYNTAX</span></span>

### <span data-ttu-id="cdfa9-105">GeoDRPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cdfa9-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdfa9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cdfa9-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdfa9-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdfa9-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdfa9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cdfa9-108">DESCRIPTION</span></span>
<span data-ttu-id="cdfa9-109">Polecenie **cmdlet New-AzServiceBusGeoDRConfiguration** Tworzy nowy alias(konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="cdfa9-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="cdfa9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cdfa9-110">EXAMPLES</span></span>

### <span data-ttu-id="cdfa9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdfa9-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="cdfa9-112">Tworzy alias "SampleDRConfigName" z podstawową przestrzenią nazw "SampleNamespace_Primary" z pomocniczą przestrzenią nazw "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="cdfa9-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="cdfa9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdfa9-113">PARAMETERS</span></span>

### <span data-ttu-id="cdfa9-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="cdfa9-114">-AlternateName</span></span>
<span data-ttu-id="cdfa9-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="cdfa9-115">AlternateName</span></span>

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

### <span data-ttu-id="cdfa9-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cdfa9-116">-AsJob</span></span>
<span data-ttu-id="cdfa9-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cdfa9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdfa9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfa9-118">-DefaultProfile</span></span>
<span data-ttu-id="cdfa9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdfa9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdfa9-120">-InputObject</span></span>
<span data-ttu-id="cdfa9-121">Obiekt Przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cdfa9-121">Namespace Object</span></span>

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

### <span data-ttu-id="cdfa9-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cdfa9-122">-Name</span></span>
<span data-ttu-id="cdfa9-123">Nazwa konfiguracji dr</span><span class="sxs-lookup"><span data-stu-id="cdfa9-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="cdfa9-124">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="cdfa9-124">-Namespace</span></span>
<span data-ttu-id="cdfa9-125">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cdfa9-125">Namespace Name</span></span>

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

### <span data-ttu-id="cdfa9-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="cdfa9-126">-PartnerNamespace</span></span>
<span data-ttu-id="cdfa9-127">Dr Configuration PartnerNamespace (ARM Id of PartnerNamespace [Pomocnicza przestrzeń nazw])</span><span class="sxs-lookup"><span data-stu-id="cdfa9-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="cdfa9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfa9-128">-ResourceGroupName</span></span>
<span data-ttu-id="cdfa9-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cdfa9-129">Resource Group Name</span></span>

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

### <span data-ttu-id="cdfa9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdfa9-130">-ResourceId</span></span>
<span data-ttu-id="cdfa9-131">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cdfa9-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="cdfa9-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdfa9-132">-Confirm</span></span>
<span data-ttu-id="cdfa9-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdfa9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdfa9-134">-WhatIf</span></span>
<span data-ttu-id="cdfa9-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdfa9-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdfa9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfa9-137">CommonParameters</span></span>
<span data-ttu-id="cdfa9-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfa9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfa9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfa9-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdfa9-140">INPUTS</span></span>

### <span data-ttu-id="cdfa9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cdfa9-141">System.String</span></span>

### <span data-ttu-id="cdfa9-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cdfa9-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="cdfa9-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cdfa9-143">OUTPUTS</span></span>

### <span data-ttu-id="cdfa9-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cdfa9-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="cdfa9-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cdfa9-145">NOTES</span></span>

## <span data-ttu-id="cdfa9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdfa9-146">RELATED LINKS</span></span>
