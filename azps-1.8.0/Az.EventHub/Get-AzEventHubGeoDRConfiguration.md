---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: a4cb60c224c440654854cff66434be1d224e8d50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709814"
---
# <span data-ttu-id="77ea5-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="77ea5-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="77ea5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="77ea5-103">Pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="77ea5-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="77ea5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77ea5-104">SYNTAX</span></span>

### <span data-ttu-id="77ea5-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77ea5-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77ea5-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="77ea5-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77ea5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77ea5-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77ea5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="77ea5-108">DESCRIPTION</span></span>
<span data-ttu-id="77ea5-109">**AzEventHubGeoDRConfiguration** pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="77ea5-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="77ea5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77ea5-110">EXAMPLES</span></span>

### <span data-ttu-id="77ea5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77ea5-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="77ea5-112">Pobiera konfigurację aliasu "SampleDRCongifName" dla podstawowego obszaru nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="77ea5-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="77ea5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77ea5-113">PARAMETERS</span></span>

### <span data-ttu-id="77ea5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ea5-114">-DefaultProfile</span></span>
<span data-ttu-id="77ea5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77ea5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77ea5-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77ea5-116">-InputObject</span></span>
<span data-ttu-id="77ea5-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="77ea5-117">Namespace Object</span></span>

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

### <span data-ttu-id="77ea5-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77ea5-118">-Name</span></span>
<span data-ttu-id="77ea5-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="77ea5-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="77ea5-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="77ea5-120">-Namespace</span></span>
<span data-ttu-id="77ea5-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="77ea5-121">Namespace Name</span></span>

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

### <span data-ttu-id="77ea5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ea5-122">-ResourceGroupName</span></span>
<span data-ttu-id="77ea5-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="77ea5-123">Resource Group Name</span></span>

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

### <span data-ttu-id="77ea5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77ea5-124">-ResourceId</span></span>
<span data-ttu-id="77ea5-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="77ea5-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="77ea5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ea5-126">CommonParameters</span></span>
<span data-ttu-id="77ea5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77ea5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ea5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ea5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ea5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77ea5-129">INPUTS</span></span>

### <span data-ttu-id="77ea5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="77ea5-130">System.String</span></span>

### <span data-ttu-id="77ea5-131">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="77ea5-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="77ea5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77ea5-132">OUTPUTS</span></span>

### <span data-ttu-id="77ea5-133">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="77ea5-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="77ea5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77ea5-134">NOTES</span></span>

## <span data-ttu-id="77ea5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77ea5-135">RELATED LINKS</span></span>
