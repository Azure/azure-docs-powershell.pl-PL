---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: 8f2651e2bfc0271964b055244995aead1b93a172
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708114"
---
# <span data-ttu-id="d33c3-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d33c3-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="d33c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d33c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d33c3-103">Umożliwia zaktualizowanie opisu istniejącej przestrzeni nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d33c3-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="d33c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d33c3-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d33c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d33c3-105">DESCRIPTION</span></span>
<span data-ttu-id="d33c3-106">Polecenie cmdlet **Set-AzServiceBusNamespace** umożliwia zaktualizowanie opisu określonego obszaru nazw magistrali usług w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d33c3-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="d33c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d33c3-107">EXAMPLES</span></span>

### <span data-ttu-id="d33c3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d33c3-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="d33c3-109">Umożliwia zaktualizowanie obszaru nazw usługi Service Bus o nowy opis.</span><span class="sxs-lookup"><span data-stu-id="d33c3-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="d33c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d33c3-110">PARAMETERS</span></span>

### <span data-ttu-id="d33c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33c3-111">-DefaultProfile</span></span>
<span data-ttu-id="d33c3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d33c3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d33c3-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d33c3-113">-Location</span></span>
<span data-ttu-id="d33c3-114">Lokalizacja obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d33c3-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="d33c3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d33c3-115">-Name</span></span>
<span data-ttu-id="d33c3-116">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="d33c3-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="d33c3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d33c3-117">-ResourceGroupName</span></span>
<span data-ttu-id="d33c3-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d33c3-118">The resource group name.</span></span>

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

### <span data-ttu-id="d33c3-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d33c3-119">-SkuCapacity</span></span>
<span data-ttu-id="d33c3-120">Pojemność SKU: przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="d33c3-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="d33c3-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d33c3-121">-SkuName</span></span>
<span data-ttu-id="d33c3-122">Nazwa SKU w obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="d33c3-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="d33c3-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="d33c3-123">-Tag</span></span>
<span data-ttu-id="d33c3-124">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d33c3-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d33c3-125">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d33c3-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d33c3-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d33c3-126">-Confirm</span></span>
<span data-ttu-id="d33c3-127">Aktualizuje obszar nazw usługi Service Bus o określonych informacjach.</span><span class="sxs-lookup"><span data-stu-id="d33c3-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="d33c3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d33c3-128">-WhatIf</span></span>
<span data-ttu-id="d33c3-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d33c3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d33c3-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d33c3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d33c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33c3-131">CommonParameters</span></span>
<span data-ttu-id="d33c3-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d33c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33c3-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d33c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33c3-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d33c3-134">INPUTS</span></span>

### <span data-ttu-id="d33c3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d33c3-135">System.String</span></span>

### <span data-ttu-id="d33c3-136">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d33c3-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d33c3-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d33c3-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d33c3-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d33c3-138">OUTPUTS</span></span>

### <span data-ttu-id="d33c3-139">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d33c3-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d33c3-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d33c3-140">NOTES</span></span>

## <span data-ttu-id="d33c3-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d33c3-141">RELATED LINKS</span></span>