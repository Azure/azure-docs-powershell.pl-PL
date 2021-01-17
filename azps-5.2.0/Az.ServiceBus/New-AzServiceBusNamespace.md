---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345466"
---
# <span data-ttu-id="f834b-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f834b-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="f834b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f834b-102">SYNOPSIS</span></span>
<span data-ttu-id="f834b-103">Tworzy nowy obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f834b-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="f834b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f834b-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f834b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f834b-105">DESCRIPTION</span></span>
<span data-ttu-id="f834b-106">Polecenie cmdlet **New-AzServiceBusNamespace** tworzy nowy obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f834b-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="f834b-107">Po utworzeniu manifest zasobów przestrzeni nazw jest niezmienny.</span><span class="sxs-lookup"><span data-stu-id="f834b-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="f834b-108">Ta operacja jest idempotent.</span><span class="sxs-lookup"><span data-stu-id="f834b-108">This operation is idempotent.</span></span>

## <span data-ttu-id="f834b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f834b-109">EXAMPLES</span></span>

### <span data-ttu-id="f834b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f834b-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="f834b-111">Tworzy nowy obszar nazw usługi Service Bus w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f834b-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="f834b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f834b-112">PARAMETERS</span></span>

### <span data-ttu-id="f834b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f834b-113">-DefaultProfile</span></span>
<span data-ttu-id="f834b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f834b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f834b-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f834b-115">-Location</span></span>
<span data-ttu-id="f834b-116">Lokalizacja obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f834b-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="f834b-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f834b-117">-Name</span></span>
<span data-ttu-id="f834b-118">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="f834b-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="f834b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f834b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f834b-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f834b-120">The resource group name.</span></span>

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

### <span data-ttu-id="f834b-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f834b-121">-SkuCapacity</span></span>
<span data-ttu-id="f834b-122">Jednostki przepływów pracy w usłudze Service Bus Premium, dozwolone wartości 1 lub 2 lub 4</span><span class="sxs-lookup"><span data-stu-id="f834b-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="f834b-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f834b-123">-SkuName</span></span>
<span data-ttu-id="f834b-124">Nazwa SKU obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f834b-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="f834b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f834b-125">-Tag</span></span>
<span data-ttu-id="f834b-126">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f834b-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="f834b-127">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f834b-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f834b-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f834b-128">-Confirm</span></span>
<span data-ttu-id="f834b-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f834b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f834b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f834b-130">-WhatIf</span></span>
<span data-ttu-id="f834b-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f834b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f834b-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f834b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f834b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f834b-133">CommonParameters</span></span>
<span data-ttu-id="f834b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f834b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f834b-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f834b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f834b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f834b-136">INPUTS</span></span>

### <span data-ttu-id="f834b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f834b-137">System.String</span></span>

### <span data-ttu-id="f834b-138">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f834b-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f834b-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f834b-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f834b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f834b-140">OUTPUTS</span></span>

### <span data-ttu-id="f834b-141">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f834b-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f834b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f834b-142">NOTES</span></span>

## <span data-ttu-id="f834b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f834b-143">RELATED LINKS</span></span>
