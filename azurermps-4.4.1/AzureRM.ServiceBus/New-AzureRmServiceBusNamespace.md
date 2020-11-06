---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552352"
---
# <span data-ttu-id="58ab6-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="58ab6-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="58ab6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="58ab6-103">Tworzy nowy obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="58ab6-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58ab6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58ab6-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ab6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58ab6-105">DESCRIPTION</span></span>
<span data-ttu-id="58ab6-106">Polecenie cmdlet **New-AzureRmServiceBusNamespace** tworzy nowy obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="58ab6-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="58ab6-107">Po utworzeniu manifest zasobów przestrzeni nazw jest niezmienny.</span><span class="sxs-lookup"><span data-stu-id="58ab6-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="58ab6-108">Ta operacja jest idempotent.</span><span class="sxs-lookup"><span data-stu-id="58ab6-108">This operation is idempotent.</span></span>

## <span data-ttu-id="58ab6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58ab6-109">EXAMPLES</span></span>

### <span data-ttu-id="58ab6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58ab6-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="58ab6-111">Tworzy nowy obszar nazw usługi Service Bus w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="58ab6-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="58ab6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58ab6-112">PARAMETERS</span></span>

### <span data-ttu-id="58ab6-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="58ab6-113">-Location</span></span>
<span data-ttu-id="58ab6-114">Lokalizacja obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="58ab6-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="58ab6-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="58ab6-115">-NamespaceName</span></span>
<span data-ttu-id="58ab6-116">Nazwa obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="58ab6-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="58ab6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ab6-117">-ResourceGroupName</span></span>
<span data-ttu-id="58ab6-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58ab6-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ab6-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="58ab6-119">-SkuName</span></span>
<span data-ttu-id="58ab6-120">Nazwa SKU obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="58ab6-120">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="58ab6-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="58ab6-121">-Tag</span></span>
<span data-ttu-id="58ab6-122">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="58ab6-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="58ab6-123">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="58ab6-123">For example:</span></span>

<span data-ttu-id="58ab6-124">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="58ab6-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="58ab6-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58ab6-125">-Confirm</span></span>
<span data-ttu-id="58ab6-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58ab6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ab6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ab6-127">-WhatIf</span></span>
<span data-ttu-id="58ab6-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58ab6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58ab6-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58ab6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ab6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ab6-130">CommonParameters</span></span>
<span data-ttu-id="58ab6-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ab6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ab6-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ab6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ab6-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58ab6-133">INPUTS</span></span>

### <span data-ttu-id="58ab6-134">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="58ab6-134">-ResourceGroup</span></span>
 <span data-ttu-id="58ab6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="58ab6-135">System.String</span></span>

### <span data-ttu-id="58ab6-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="58ab6-136">-NamespaceName</span></span>
 <span data-ttu-id="58ab6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="58ab6-137">System.String</span></span>

### <span data-ttu-id="58ab6-138">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="58ab6-138">-Location</span></span>
 <span data-ttu-id="58ab6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="58ab6-139">System.String</span></span>

### <span data-ttu-id="58ab6-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="58ab6-140">-SkuName</span></span>
 <span data-ttu-id="58ab6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="58ab6-141">System.String</span></span>

### <span data-ttu-id="58ab6-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="58ab6-142">-Tag</span></span>
 <span data-ttu-id="58ab6-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="58ab6-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="58ab6-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58ab6-144">OUTPUTS</span></span>

### <span data-ttu-id="58ab6-145">Microsoft. Azure. Commands. ServiceBus. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="58ab6-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="58ab6-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58ab6-146">NOTES</span></span>

## <span data-ttu-id="58ab6-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58ab6-147">RELATED LINKS</span></span>
