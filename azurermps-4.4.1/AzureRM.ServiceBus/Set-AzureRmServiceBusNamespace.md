---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 134e0d20566a8310a381a38297984202b7509250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718988"
---
# <span data-ttu-id="a0e47-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a0e47-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="a0e47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0e47-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e47-103">Umożliwia zaktualizowanie opisu istniejącej przestrzeni nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a0e47-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0e47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0e47-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> -Name <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0e47-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0e47-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e47-106">Polecenie cmdlet **Set-AzureRmServiceBusNamespace** umożliwia zaktualizowanie opisu określonego obszaru nazw magistrali usług w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0e47-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="a0e47-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0e47-107">EXAMPLES</span></span>

### <span data-ttu-id="a0e47-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0e47-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
Status             :
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
Enabled            : False
```

<span data-ttu-id="a0e47-109">Umożliwia zaktualizowanie obszaru nazw usługi Service Bus o nowy opis.</span><span class="sxs-lookup"><span data-stu-id="a0e47-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="a0e47-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0e47-110">PARAMETERS</span></span>

### <span data-ttu-id="a0e47-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a0e47-111">-Location</span></span>
<span data-ttu-id="a0e47-112">Lokalizacja obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a0e47-112">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e47-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e47-113">-ResourceGroupName</span></span>
<span data-ttu-id="a0e47-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0e47-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e47-115">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a0e47-115">-SkuCapacity</span></span>
<span data-ttu-id="a0e47-116">Pojemność SKU: przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="a0e47-116">Namespace Sku Capacity.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e47-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a0e47-117">-SkuName</span></span>
<span data-ttu-id="a0e47-118">Nazwa SKU w obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="a0e47-118">The namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e47-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0e47-119">-Tag</span></span>
<span data-ttu-id="a0e47-120">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a0e47-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a0e47-121">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a0e47-121">For example:</span></span>

<span data-ttu-id="a0e47-122">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a0e47-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e47-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0e47-123">-Confirm</span></span>
<span data-ttu-id="a0e47-124">Aktualizuje obszar nazw usługi Service Bus o określonych informacjach.</span><span class="sxs-lookup"><span data-stu-id="a0e47-124">Updates the Service Bus namespace with the specified information.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e47-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e47-125">-WhatIf</span></span>
<span data-ttu-id="a0e47-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0e47-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e47-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0e47-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e47-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e47-128">-DefaultProfile</span></span>
<span data-ttu-id="a0e47-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e47-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0e47-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0e47-130">-Name</span></span>
<span data-ttu-id="a0e47-131">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="a0e47-131">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e47-132">CommonParameters</span></span>
<span data-ttu-id="a0e47-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e47-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0e47-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e47-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0e47-135">INPUTS</span></span>

### <span data-ttu-id="a0e47-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a0e47-136">-ResourceGroup</span></span>
 <span data-ttu-id="a0e47-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a0e47-137">System.String</span></span>

### <span data-ttu-id="a0e47-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a0e47-138">-NamespaceName</span></span>
 <span data-ttu-id="a0e47-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a0e47-139">System.String</span></span>

### <span data-ttu-id="a0e47-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a0e47-140">-Location</span></span>
 <span data-ttu-id="a0e47-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a0e47-141">System.String</span></span>

### <span data-ttu-id="a0e47-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a0e47-142">-SkuName</span></span>
 <span data-ttu-id="a0e47-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a0e47-143">System.String</span></span>

### <span data-ttu-id="a0e47-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0e47-144">-Tag</span></span>
 <span data-ttu-id="a0e47-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a0e47-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a0e47-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0e47-146">OUTPUTS</span></span>

### <span data-ttu-id="a0e47-147">Microsoft. Azure. Commands. ServiceBus. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a0e47-147">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="a0e47-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0e47-148">NOTES</span></span>
## <span data-ttu-id="a0e47-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0e47-149">RELATED LINKS</span></span>

## <span data-ttu-id="a0e47-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0e47-150">RELATED LINKS</span></span>

