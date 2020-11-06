---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542291"
---
# <span data-ttu-id="994ee-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="994ee-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="994ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="994ee-102">SYNOPSIS</span></span>
<span data-ttu-id="994ee-103">Pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="994ee-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="994ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="994ee-104">SYNTAX</span></span>

### <span data-ttu-id="994ee-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="994ee-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="994ee-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="994ee-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="994ee-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="994ee-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="994ee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="994ee-108">DESCRIPTION</span></span>
<span data-ttu-id="994ee-109">**AzureRmServiceBusGeoDRConfiguration** pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="994ee-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="994ee-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="994ee-110">EXAMPLES</span></span>

### <span data-ttu-id="994ee-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="994ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="994ee-112">Pobiera konfigurację aliasu "SampleDRCongifName" dla podstawowego obszaru nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="994ee-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="994ee-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="994ee-113">PARAMETERS</span></span>

### <span data-ttu-id="994ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994ee-114">-DefaultProfile</span></span>
<span data-ttu-id="994ee-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="994ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="994ee-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="994ee-116">-InputObject</span></span>
<span data-ttu-id="994ee-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="994ee-117">Namespace Object</span></span>

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

### <span data-ttu-id="994ee-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="994ee-118">-Name</span></span>
<span data-ttu-id="994ee-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="994ee-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994ee-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="994ee-120">-Namespace</span></span>
<span data-ttu-id="994ee-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="994ee-121">Namespace Name</span></span>

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

### <span data-ttu-id="994ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="994ee-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="994ee-123">Resource Group Name</span></span>

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

### <span data-ttu-id="994ee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="994ee-124">-ResourceId</span></span>
<span data-ttu-id="994ee-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="994ee-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994ee-126">CommonParameters</span></span>
<span data-ttu-id="994ee-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="994ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="994ee-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="994ee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994ee-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="994ee-129">INPUTS</span></span>

### <span data-ttu-id="994ee-130">System. String</span><span class="sxs-lookup"><span data-stu-id="994ee-130">System.String</span></span>
<span data-ttu-id="994ee-131">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="994ee-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="994ee-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="994ee-132">OUTPUTS</span></span>

### <span data-ttu-id="994ee-133">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. PSServiceBusDRConfigurationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="994ee-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="994ee-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="994ee-134">NOTES</span></span>

## <span data-ttu-id="994ee-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="994ee-135">RELATED LINKS</span></span>
