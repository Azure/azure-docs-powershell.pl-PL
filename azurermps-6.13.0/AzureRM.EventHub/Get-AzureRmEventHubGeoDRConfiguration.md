---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 40a80a975de56a867f0dcbc34aea0e46d42a155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543843"
---
# <span data-ttu-id="92d63-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="92d63-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="92d63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92d63-102">SYNOPSIS</span></span>
<span data-ttu-id="92d63-103">Pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="92d63-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92d63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92d63-104">SYNTAX</span></span>

### <span data-ttu-id="92d63-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92d63-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92d63-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="92d63-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92d63-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92d63-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d63-108">Opis</span><span class="sxs-lookup"><span data-stu-id="92d63-108">DESCRIPTION</span></span>
<span data-ttu-id="92d63-109">**AzureRmEventHubGeoDRConfiguration** pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="92d63-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="92d63-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92d63-110">EXAMPLES</span></span>

### <span data-ttu-id="92d63-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92d63-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="92d63-112">Pobiera konfigurację aliasu "SampleDRCongifName" dla podstawowego obszaru nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="92d63-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="92d63-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92d63-113">PARAMETERS</span></span>

### <span data-ttu-id="92d63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d63-114">-DefaultProfile</span></span>
<span data-ttu-id="92d63-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92d63-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d63-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="92d63-116">-InputObject</span></span>
<span data-ttu-id="92d63-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="92d63-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92d63-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92d63-118">-Name</span></span>
<span data-ttu-id="92d63-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="92d63-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="92d63-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="92d63-120">-Namespace</span></span>
<span data-ttu-id="92d63-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="92d63-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92d63-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d63-122">-ResourceGroupName</span></span>
<span data-ttu-id="92d63-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="92d63-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92d63-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92d63-124">-ResourceId</span></span>
<span data-ttu-id="92d63-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="92d63-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92d63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d63-126">CommonParameters</span></span>
<span data-ttu-id="92d63-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d63-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d63-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d63-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92d63-129">INPUTS</span></span>

### <span data-ttu-id="92d63-130">System. String</span><span class="sxs-lookup"><span data-stu-id="92d63-130">System.String</span></span>

### <span data-ttu-id="92d63-131">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="92d63-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="92d63-132">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92d63-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="92d63-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92d63-133">OUTPUTS</span></span>

### <span data-ttu-id="92d63-134">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="92d63-134">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="92d63-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92d63-135">NOTES</span></span>

## <span data-ttu-id="92d63-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92d63-136">RELATED LINKS</span></span>
