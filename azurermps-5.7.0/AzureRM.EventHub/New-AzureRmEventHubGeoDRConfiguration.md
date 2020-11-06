---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: feeb47a1db28debfcfeb4e5d61c22e15db66b799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528141"
---
# <span data-ttu-id="e3d69-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3d69-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="e3d69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3d69-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d69-103">Tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="e3d69-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3d69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3d69-104">SYNTAX</span></span>

### <span data-ttu-id="e3d69-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e3d69-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d69-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3d69-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d69-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3d69-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3d69-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e3d69-108">DESCRIPTION</span></span>
<span data-ttu-id="e3d69-109">Polecenie cmdlet **New-AzureRmEventHubGeoDRConfiguration** tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="e3d69-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="e3d69-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3d69-110">EXAMPLES</span></span>

### <span data-ttu-id="e3d69-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3d69-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="e3d69-112">Tworzy alias "SampleDRCongifName" z podstawowym obszarem nazw "SampleNamespace_Primary" z pomocniczym obszarem nazw "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="e3d69-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="e3d69-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3d69-113">PARAMETERS</span></span>

### <span data-ttu-id="e3d69-114">-Symbol alternatywny</span><span class="sxs-lookup"><span data-stu-id="e3d69-114">-AlternateName</span></span>
<span data-ttu-id="e3d69-115">Symbol zastępczy wymagany, gdy nazwa konfiguracji DR jest taka sama jak główna przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="e3d69-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d69-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3d69-116">-AsJob</span></span>
<span data-ttu-id="e3d69-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e3d69-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3d69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d69-118">-DefaultProfile</span></span>
<span data-ttu-id="e3d69-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d69-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d69-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e3d69-120">-InputObject</span></span>
<span data-ttu-id="e3d69-121">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="e3d69-121">Namespace Object</span></span>

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

### <span data-ttu-id="e3d69-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3d69-122">-Name</span></span>
<span data-ttu-id="e3d69-123">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="e3d69-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="e3d69-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e3d69-124">-Namespace</span></span>
<span data-ttu-id="e3d69-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="e3d69-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d69-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="e3d69-126">-PartnerNamespace</span></span>
<span data-ttu-id="e3d69-127">PartnerNamespace konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="e3d69-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="e3d69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d69-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3d69-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e3d69-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d69-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3d69-130">-ResourceId</span></span>
<span data-ttu-id="e3d69-131">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="e3d69-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="e3d69-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3d69-132">-Confirm</span></span>
<span data-ttu-id="e3d69-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3d69-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d69-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d69-134">-WhatIf</span></span>
<span data-ttu-id="e3d69-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3d69-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d69-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3d69-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d69-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d69-137">CommonParameters</span></span>
<span data-ttu-id="e3d69-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d69-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e3d69-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d69-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d69-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3d69-140">INPUTS</span></span>

### <span data-ttu-id="e3d69-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e3d69-141">System.String</span></span>
<span data-ttu-id="e3d69-142">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e3d69-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="e3d69-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3d69-143">OUTPUTS</span></span>

### <span data-ttu-id="e3d69-144">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e3d69-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="e3d69-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3d69-145">NOTES</span></span>

## <span data-ttu-id="e3d69-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3d69-146">RELATED LINKS</span></span>
