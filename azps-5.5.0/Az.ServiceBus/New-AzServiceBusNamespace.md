---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197858"
---
# <span data-ttu-id="be802-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="be802-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="be802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be802-102">SYNOPSIS</span></span>
<span data-ttu-id="be802-103">Tworzy nową przestrzeń nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="be802-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="be802-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be802-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be802-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="be802-105">DESCRIPTION</span></span>
<span data-ttu-id="be802-106">Polecenie **cmdlet New-AzServiceBusNamespace** tworzy nową przestrzeń nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="be802-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="be802-107">Po utworzeniu manifestu zasobu przestrzeni nazw jest nieumiejętny.</span><span class="sxs-lookup"><span data-stu-id="be802-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="be802-108">Ta operacja jest idempotentna.</span><span class="sxs-lookup"><span data-stu-id="be802-108">This operation is idempotent.</span></span>

## <span data-ttu-id="be802-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be802-109">EXAMPLES</span></span>

### <span data-ttu-id="be802-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be802-110">Example 1</span></span>
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

<span data-ttu-id="be802-111">Tworzy nową przestrzeń nazw autobusu usług w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be802-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="be802-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be802-112">PARAMETERS</span></span>

### <span data-ttu-id="be802-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be802-113">-DefaultProfile</span></span>
<span data-ttu-id="be802-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be802-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be802-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="be802-115">-Location</span></span>
<span data-ttu-id="be802-116">Lokalizacja przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="be802-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="be802-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="be802-117">-Name</span></span>
<span data-ttu-id="be802-118">Nazwa przestrzeni nazw usługi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="be802-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="be802-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be802-119">-ResourceGroupName</span></span>
<span data-ttu-id="be802-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be802-120">The resource group name.</span></span>

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

### <span data-ttu-id="be802-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="be802-121">-SkuCapacity</span></span>
<span data-ttu-id="be802-122">Jednostki przepływności przestrzeni nazw typu Premium usługi, dozwolone wartości 1 lub 2 lub 4</span><span class="sxs-lookup"><span data-stu-id="be802-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="be802-123">-SKUName</span><span class="sxs-lookup"><span data-stu-id="be802-123">-SkuName</span></span>
<span data-ttu-id="be802-124">Nazwa SKU przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="be802-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="be802-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="be802-125">-Tag</span></span>
<span data-ttu-id="be802-126">Pary klucz-wartość w postaci tabeli skrótów ustawionej jako tagi na serwerze.</span><span class="sxs-lookup"><span data-stu-id="be802-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="be802-127">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="be802-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="be802-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be802-128">-Confirm</span></span>
<span data-ttu-id="be802-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be802-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be802-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be802-130">-WhatIf</span></span>
<span data-ttu-id="be802-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be802-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be802-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="be802-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be802-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be802-133">CommonParameters</span></span>
<span data-ttu-id="be802-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be802-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be802-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be802-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be802-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be802-136">INPUTS</span></span>

### <span data-ttu-id="be802-137">System.String</span><span class="sxs-lookup"><span data-stu-id="be802-137">System.String</span></span>

### <span data-ttu-id="be802-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="be802-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="be802-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="be802-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="be802-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be802-140">OUTPUTS</span></span>

### <span data-ttu-id="be802-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="be802-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="be802-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be802-142">NOTES</span></span>

## <span data-ttu-id="be802-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be802-143">RELATED LINKS</span></span>
