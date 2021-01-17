---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323587"
---
# <span data-ttu-id="969e7-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="969e7-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="969e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="969e7-102">SYNOPSIS</span></span>
<span data-ttu-id="969e7-103">Pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="969e7-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="969e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="969e7-104">SYNTAX</span></span>

### <span data-ttu-id="969e7-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="969e7-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="969e7-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="969e7-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="969e7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="969e7-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="969e7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="969e7-108">DESCRIPTION</span></span>
<span data-ttu-id="969e7-109">**AzEventHubGeoDRConfiguration** pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="969e7-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="969e7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="969e7-110">EXAMPLES</span></span>

### <span data-ttu-id="969e7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="969e7-111">Example 1</span></span>
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

<span data-ttu-id="969e7-112">Pobiera konfigurację aliasu "SampleDRConfigName" dla podstawowego obszaru nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="969e7-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="969e7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="969e7-113">PARAMETERS</span></span>

### <span data-ttu-id="969e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969e7-114">-DefaultProfile</span></span>
<span data-ttu-id="969e7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="969e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="969e7-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="969e7-116">-InputObject</span></span>
<span data-ttu-id="969e7-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="969e7-117">Namespace Object</span></span>

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

### <span data-ttu-id="969e7-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="969e7-118">-Name</span></span>
<span data-ttu-id="969e7-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="969e7-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="969e7-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="969e7-120">-Namespace</span></span>
<span data-ttu-id="969e7-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="969e7-121">Namespace Name</span></span>

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

### <span data-ttu-id="969e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="969e7-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="969e7-123">Resource Group Name</span></span>

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

### <span data-ttu-id="969e7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="969e7-124">-ResourceId</span></span>
<span data-ttu-id="969e7-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="969e7-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="969e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969e7-126">CommonParameters</span></span>
<span data-ttu-id="969e7-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969e7-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969e7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969e7-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="969e7-129">INPUTS</span></span>

### <span data-ttu-id="969e7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="969e7-130">System.String</span></span>

### <span data-ttu-id="969e7-131">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="969e7-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="969e7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="969e7-132">OUTPUTS</span></span>

### <span data-ttu-id="969e7-133">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="969e7-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="969e7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="969e7-134">NOTES</span></span>

## <span data-ttu-id="969e7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="969e7-135">RELATED LINKS</span></span>
