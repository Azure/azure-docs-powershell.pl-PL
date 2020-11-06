---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: b90144fb94dcef874ce67168364aa65782084b4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551580"
---
# <span data-ttu-id="f02a4-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f02a4-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="f02a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f02a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f02a4-103">Tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="f02a4-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f02a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f02a4-104">SYNTAX</span></span>

### <span data-ttu-id="f02a4-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f02a4-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f02a4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f02a4-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f02a4-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f02a4-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f02a4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f02a4-108">DESCRIPTION</span></span>
<span data-ttu-id="f02a4-109">Polecenie cmdlet **New-AzureRmServiceBusGeoDRConfiguration** tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="f02a4-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f02a4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f02a4-110">EXAMPLES</span></span>

### <span data-ttu-id="f02a4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f02a4-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="f02a4-112">Tworzy alias "SampleDRCongifName" z podstawowym obszarem nazw "SampleNamespace_Primary" z pomocniczym obszarem nazw "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="f02a4-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="f02a4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f02a4-113">PARAMETERS</span></span>

### <span data-ttu-id="f02a4-114">-Symbol alternatywny</span><span class="sxs-lookup"><span data-stu-id="f02a4-114">-AlternateName</span></span>
<span data-ttu-id="f02a4-115">Symbol zastępczy</span><span class="sxs-lookup"><span data-stu-id="f02a4-115">AlternateName</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02a4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f02a4-116">-AsJob</span></span>
<span data-ttu-id="f02a4-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f02a4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f02a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02a4-118">-DefaultProfile</span></span>
<span data-ttu-id="f02a4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f02a4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f02a4-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f02a4-120">-InputObject</span></span>
<span data-ttu-id="f02a4-121">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="f02a4-121">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f02a4-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f02a4-122">-Name</span></span>
<span data-ttu-id="f02a4-123">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="f02a4-123">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02a4-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f02a4-124">-Namespace</span></span>
<span data-ttu-id="f02a4-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="f02a4-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02a4-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="f02a4-126">-PartnerNamespace</span></span>
<span data-ttu-id="f02a4-127">DR Configuration PartnerNamespace (identyfikator ARM PartnerNamespace [pomocnicza przestrzeń nazw])</span><span class="sxs-lookup"><span data-stu-id="f02a4-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02a4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f02a4-128">-ResourceGroupName</span></span>
<span data-ttu-id="f02a4-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f02a4-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02a4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f02a4-130">-ResourceId</span></span>
<span data-ttu-id="f02a4-131">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="f02a4-131">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02a4-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f02a4-132">-Confirm</span></span>
<span data-ttu-id="f02a4-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f02a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f02a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f02a4-134">-WhatIf</span></span>
<span data-ttu-id="f02a4-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f02a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f02a4-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f02a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f02a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02a4-137">CommonParameters</span></span>
<span data-ttu-id="f02a4-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f02a4-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f02a4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02a4-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f02a4-140">INPUTS</span></span>

### <span data-ttu-id="f02a4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f02a4-141">System.String</span></span>
<span data-ttu-id="f02a4-142">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f02a4-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="f02a4-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f02a4-143">OUTPUTS</span></span>

### <span data-ttu-id="f02a4-144">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f02a4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="f02a4-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f02a4-145">NOTES</span></span>

## <span data-ttu-id="f02a4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f02a4-146">RELATED LINKS</span></span>
