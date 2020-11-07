---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 6ac46fc8b8f94480e11f00d44efc690d97ee56a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718267"
---
# <span data-ttu-id="ca6af-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ca6af-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="ca6af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca6af-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6af-103">Umożliwia zaktualizowanie opisu istniejącej przestrzeni nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="ca6af-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca6af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca6af-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca6af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca6af-105">DESCRIPTION</span></span>
<span data-ttu-id="ca6af-106">Polecenie cmdlet **Set-AzureRmServiceBusNamespace** umożliwia zaktualizowanie opisu określonego obszaru nazw magistrali usług w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca6af-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="ca6af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca6af-107">EXAMPLES</span></span>

### <span data-ttu-id="ca6af-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca6af-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="ca6af-109">Umożliwia zaktualizowanie obszaru nazw usługi Service Bus o nowy opis.</span><span class="sxs-lookup"><span data-stu-id="ca6af-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="ca6af-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca6af-110">PARAMETERS</span></span>

### <span data-ttu-id="ca6af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6af-111">-DefaultProfile</span></span>
<span data-ttu-id="ca6af-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca6af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca6af-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ca6af-113">-Location</span></span>
<span data-ttu-id="ca6af-114">Lokalizacja obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="ca6af-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="ca6af-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca6af-115">-Name</span></span>
<span data-ttu-id="ca6af-116">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="ca6af-116">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca6af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca6af-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca6af-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca6af-118">The resource group name.</span></span>

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

### <span data-ttu-id="ca6af-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ca6af-119">-SkuCapacity</span></span>
<span data-ttu-id="ca6af-120">Pojemność SKU: przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="ca6af-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="ca6af-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ca6af-121">-SkuName</span></span>
<span data-ttu-id="ca6af-122">Nazwa SKU w obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="ca6af-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="ca6af-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca6af-123">-Tag</span></span>
<span data-ttu-id="ca6af-124">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ca6af-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ca6af-125">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ca6af-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ca6af-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca6af-126">-Confirm</span></span>
<span data-ttu-id="ca6af-127">Aktualizuje obszar nazw usługi Service Bus o określonych informacjach.</span><span class="sxs-lookup"><span data-stu-id="ca6af-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="ca6af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca6af-128">-WhatIf</span></span>
<span data-ttu-id="ca6af-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca6af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca6af-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca6af-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca6af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6af-131">CommonParameters</span></span>
<span data-ttu-id="ca6af-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6af-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca6af-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6af-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca6af-134">INPUTS</span></span>

### <span data-ttu-id="ca6af-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ca6af-135">System.String</span></span>

### <span data-ttu-id="ca6af-136">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ca6af-136">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ca6af-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca6af-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca6af-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca6af-138">OUTPUTS</span></span>

### <span data-ttu-id="ca6af-139">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ca6af-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ca6af-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca6af-140">NOTES</span></span>

## <span data-ttu-id="ca6af-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca6af-141">RELATED LINKS</span></span>
