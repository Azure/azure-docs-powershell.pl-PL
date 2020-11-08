---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221752"
---
# <span data-ttu-id="c8ab1-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8ab1-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="c8ab1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ab1-103">Pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c8ab1-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c8ab1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8ab1-104">SYNTAX</span></span>

### <span data-ttu-id="c8ab1-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c8ab1-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8ab1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c8ab1-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8ab1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8ab1-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8ab1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c8ab1-108">DESCRIPTION</span></span>
<span data-ttu-id="c8ab1-109">**AzEventHubGeoDRConfiguration** pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c8ab1-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c8ab1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8ab1-110">EXAMPLES</span></span>

### <span data-ttu-id="c8ab1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8ab1-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="c8ab1-112">Pobiera konfigurację aliasu "SampleDRConfigName" dla podstawowego obszaru nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="c8ab1-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="c8ab1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8ab1-113">PARAMETERS</span></span>

### <span data-ttu-id="c8ab1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ab1-114">-DefaultProfile</span></span>
<span data-ttu-id="c8ab1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8ab1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8ab1-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8ab1-116">-InputObject</span></span>
<span data-ttu-id="c8ab1-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ab1-117">Namespace Object</span></span>

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

### <span data-ttu-id="c8ab1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8ab1-118">-Name</span></span>
<span data-ttu-id="c8ab1-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="c8ab1-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c8ab1-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ab1-120">-Namespace</span></span>
<span data-ttu-id="c8ab1-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c8ab1-121">Namespace Name</span></span>

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

### <span data-ttu-id="c8ab1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8ab1-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8ab1-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c8ab1-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c8ab1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8ab1-124">-ResourceId</span></span>
<span data-ttu-id="c8ab1-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c8ab1-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c8ab1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ab1-126">CommonParameters</span></span>
<span data-ttu-id="c8ab1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8ab1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ab1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8ab1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ab1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8ab1-129">INPUTS</span></span>

### <span data-ttu-id="c8ab1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c8ab1-130">System.String</span></span>

### <span data-ttu-id="c8ab1-131">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c8ab1-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c8ab1-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8ab1-132">OUTPUTS</span></span>

### <span data-ttu-id="c8ab1-133">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c8ab1-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="c8ab1-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8ab1-134">NOTES</span></span>

## <span data-ttu-id="c8ab1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8ab1-135">RELATED LINKS</span></span>
