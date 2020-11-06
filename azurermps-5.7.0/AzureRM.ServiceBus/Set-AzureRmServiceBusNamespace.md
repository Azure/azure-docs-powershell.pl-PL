---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: f4a94823ba0ff615a68a9e17703ba7e8193b0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547951"
---
# <span data-ttu-id="31a52-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="31a52-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="31a52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31a52-102">SYNOPSIS</span></span>
<span data-ttu-id="31a52-103">Umożliwia zaktualizowanie opisu istniejącej przestrzeni nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="31a52-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31a52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31a52-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a52-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31a52-105">DESCRIPTION</span></span>
<span data-ttu-id="31a52-106">Polecenie cmdlet **Set-AzureRmServiceBusNamespace** umożliwia zaktualizowanie opisu określonego obszaru nazw magistrali usług w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="31a52-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="31a52-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31a52-107">EXAMPLES</span></span>

### <span data-ttu-id="31a52-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31a52-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="31a52-109">Umożliwia zaktualizowanie obszaru nazw usługi Service Bus o nowy opis.</span><span class="sxs-lookup"><span data-stu-id="31a52-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="31a52-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31a52-110">PARAMETERS</span></span>

### <span data-ttu-id="31a52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a52-111">-DefaultProfile</span></span>
<span data-ttu-id="31a52-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31a52-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a52-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="31a52-113">-Location</span></span>
<span data-ttu-id="31a52-114">Lokalizacja obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="31a52-114">The Service Bus namespace location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a52-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31a52-115">-Name</span></span>
<span data-ttu-id="31a52-116">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="31a52-116">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a52-117">-ResourceGroupName</span></span>
<span data-ttu-id="31a52-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="31a52-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a52-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="31a52-119">-SkuCapacity</span></span>
<span data-ttu-id="31a52-120">Pojemność SKU: przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="31a52-120">Namespace Sku Capacity.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a52-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="31a52-121">-SkuName</span></span>
<span data-ttu-id="31a52-122">Nazwa SKU w obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="31a52-122">The namespace SKU name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a52-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="31a52-123">-Tag</span></span>
<span data-ttu-id="31a52-124">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="31a52-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31a52-125">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="31a52-125">For example:</span></span>

<span data-ttu-id="31a52-126">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="31a52-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a52-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31a52-127">-Confirm</span></span>
<span data-ttu-id="31a52-128">Aktualizuje obszar nazw usługi Service Bus o określonych informacjach.</span><span class="sxs-lookup"><span data-stu-id="31a52-128">Updates the Service Bus namespace with the specified information.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a52-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a52-129">-WhatIf</span></span>
<span data-ttu-id="31a52-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31a52-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31a52-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31a52-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a52-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a52-132">CommonParameters</span></span>
<span data-ttu-id="31a52-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a52-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a52-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a52-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a52-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31a52-135">INPUTS</span></span>

### <span data-ttu-id="31a52-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="31a52-136">-ResourceGroup</span></span>
 <span data-ttu-id="31a52-137">System. String</span><span class="sxs-lookup"><span data-stu-id="31a52-137">System.String</span></span>

### <span data-ttu-id="31a52-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="31a52-138">-NamespaceName</span></span>
 <span data-ttu-id="31a52-139">System. String</span><span class="sxs-lookup"><span data-stu-id="31a52-139">System.String</span></span>

### <span data-ttu-id="31a52-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="31a52-140">-Location</span></span>
 <span data-ttu-id="31a52-141">System. String</span><span class="sxs-lookup"><span data-stu-id="31a52-141">System.String</span></span>

### <span data-ttu-id="31a52-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="31a52-142">-SkuName</span></span>
 <span data-ttu-id="31a52-143">System. String</span><span class="sxs-lookup"><span data-stu-id="31a52-143">System.String</span></span>

### <span data-ttu-id="31a52-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="31a52-144">-Tag</span></span>
 <span data-ttu-id="31a52-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="31a52-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="31a52-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31a52-146">OUTPUTS</span></span>

### <span data-ttu-id="31a52-147">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="31a52-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="31a52-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31a52-148">NOTES</span></span>


## <span data-ttu-id="31a52-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31a52-149">RELATED LINKS</span></span>

