---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: f1edc3f65747203a587de82c9f03ce79b258cd36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981658"
---
# <span data-ttu-id="fbe69-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="fbe69-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="fbe69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe69-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe69-103">Aktualizuje opis istniejącej przestrzeni nazw typu Service Bus.</span><span class="sxs-lookup"><span data-stu-id="fbe69-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="fbe69-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbe69-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe69-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbe69-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe69-106">Polecenie **cmdlet Set-AzServiceBusNamespace** aktualizuje opis określonej przestrzeni nazw typu Service Bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbe69-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="fbe69-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbe69-107">EXAMPLES</span></span>

### <span data-ttu-id="fbe69-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fbe69-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="fbe69-109">Aktualizuje przestrzeń nazw typu service bus o nowy opis.</span><span class="sxs-lookup"><span data-stu-id="fbe69-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="fbe69-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbe69-110">PARAMETERS</span></span>

### <span data-ttu-id="fbe69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe69-111">-DefaultProfile</span></span>
<span data-ttu-id="fbe69-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe69-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbe69-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fbe69-113">-Location</span></span>
<span data-ttu-id="fbe69-114">Lokalizacja przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="fbe69-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="fbe69-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fbe69-115">-Name</span></span>
<span data-ttu-id="fbe69-116">Nazwa przestrzeni nazw usługi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="fbe69-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="fbe69-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe69-117">-ResourceGroupName</span></span>
<span data-ttu-id="fbe69-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbe69-118">The resource group name.</span></span>

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

### <span data-ttu-id="fbe69-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fbe69-119">-SkuCapacity</span></span>
<span data-ttu-id="fbe69-120">Pojemność sku przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="fbe69-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="fbe69-121">-SKUName</span><span class="sxs-lookup"><span data-stu-id="fbe69-121">-SkuName</span></span>
<span data-ttu-id="fbe69-122">Nazwa SKU przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="fbe69-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="fbe69-123">— Tag</span><span class="sxs-lookup"><span data-stu-id="fbe69-123">-Tag</span></span>
<span data-ttu-id="fbe69-124">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="fbe69-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fbe69-125">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fbe69-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fbe69-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbe69-126">-Confirm</span></span>
<span data-ttu-id="fbe69-127">Aktualizuje przestrzeń nazw autobusu usług o określone informacje.</span><span class="sxs-lookup"><span data-stu-id="fbe69-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="fbe69-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe69-128">-WhatIf</span></span>
<span data-ttu-id="fbe69-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe69-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe69-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fbe69-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe69-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe69-131">CommonParameters</span></span>
<span data-ttu-id="fbe69-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe69-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe69-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe69-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe69-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe69-134">INPUTS</span></span>

### <span data-ttu-id="fbe69-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe69-135">System.String</span></span>

### <span data-ttu-id="fbe69-136">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fbe69-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fbe69-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbe69-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fbe69-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe69-138">OUTPUTS</span></span>

### <span data-ttu-id="fbe69-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fbe69-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="fbe69-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbe69-140">NOTES</span></span>

## <span data-ttu-id="fbe69-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbe69-141">RELATED LINKS</span></span>
