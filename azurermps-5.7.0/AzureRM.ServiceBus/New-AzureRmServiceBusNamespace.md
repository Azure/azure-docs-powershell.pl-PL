---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547980"
---
# <span data-ttu-id="90221-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="90221-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="90221-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90221-102">SYNOPSIS</span></span>
<span data-ttu-id="90221-103">Tworzy nowy obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="90221-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90221-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90221-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90221-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90221-105">DESCRIPTION</span></span>
<span data-ttu-id="90221-106">Polecenie cmdlet **New-AzureRmServiceBusNamespace** tworzy nowy obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="90221-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="90221-107">Po utworzeniu manifest zasobów przestrzeni nazw jest niezmienny.</span><span class="sxs-lookup"><span data-stu-id="90221-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="90221-108">Ta operacja jest idempotent.</span><span class="sxs-lookup"><span data-stu-id="90221-108">This operation is idempotent.</span></span>

## <span data-ttu-id="90221-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90221-109">EXAMPLES</span></span>

### <span data-ttu-id="90221-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90221-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="90221-111">Tworzy nowy obszar nazw usługi Service Bus w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="90221-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="90221-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90221-112">PARAMETERS</span></span>

### <span data-ttu-id="90221-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90221-113">-DefaultProfile</span></span>
<span data-ttu-id="90221-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90221-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90221-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="90221-115">-Location</span></span>
<span data-ttu-id="90221-116">Lokalizacja obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="90221-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="90221-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90221-117">-Name</span></span>
<span data-ttu-id="90221-118">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="90221-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="90221-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90221-119">-ResourceGroupName</span></span>
<span data-ttu-id="90221-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90221-120">The resource group name.</span></span>

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

### <span data-ttu-id="90221-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="90221-121">-SkuName</span></span>
<span data-ttu-id="90221-122">Nazwa SKU obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="90221-122">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="90221-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="90221-123">-Tag</span></span>
<span data-ttu-id="90221-124">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="90221-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="90221-125">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="90221-125">For example:</span></span>

<span data-ttu-id="90221-126">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="90221-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="90221-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90221-127">-Confirm</span></span>
<span data-ttu-id="90221-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90221-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90221-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90221-129">-WhatIf</span></span>
<span data-ttu-id="90221-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90221-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90221-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90221-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90221-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90221-132">CommonParameters</span></span>
<span data-ttu-id="90221-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90221-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90221-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90221-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90221-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90221-135">INPUTS</span></span>

### <span data-ttu-id="90221-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="90221-136">-ResourceGroup</span></span>
 <span data-ttu-id="90221-137">System. String</span><span class="sxs-lookup"><span data-stu-id="90221-137">System.String</span></span>

### <span data-ttu-id="90221-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="90221-138">-NamespaceName</span></span>
 <span data-ttu-id="90221-139">System. String</span><span class="sxs-lookup"><span data-stu-id="90221-139">System.String</span></span>

### <span data-ttu-id="90221-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="90221-140">-Location</span></span>
 <span data-ttu-id="90221-141">System. String</span><span class="sxs-lookup"><span data-stu-id="90221-141">System.String</span></span>

### <span data-ttu-id="90221-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="90221-142">-SkuName</span></span>
 <span data-ttu-id="90221-143">System. String</span><span class="sxs-lookup"><span data-stu-id="90221-143">System.String</span></span>

### <span data-ttu-id="90221-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="90221-144">-Tag</span></span>
 <span data-ttu-id="90221-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90221-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90221-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90221-146">OUTPUTS</span></span>

### <span data-ttu-id="90221-147">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="90221-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="90221-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90221-148">NOTES</span></span>

## <span data-ttu-id="90221-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90221-149">RELATED LINKS</span></span>

