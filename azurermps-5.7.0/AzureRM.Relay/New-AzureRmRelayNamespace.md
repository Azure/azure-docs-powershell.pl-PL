---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548028"
---
# <span data-ttu-id="01d18-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="01d18-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="01d18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01d18-102">SYNOPSIS</span></span>
<span data-ttu-id="01d18-103">Tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="01d18-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01d18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01d18-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01d18-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01d18-105">DESCRIPTION</span></span>
<span data-ttu-id="01d18-106">Polecenie cmdlet **New-AzureRmRelayNamespace** tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="01d18-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="01d18-107">Po utworzeniu manifest zasobów przestrzeni nazw jest niezmienny.</span><span class="sxs-lookup"><span data-stu-id="01d18-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="01d18-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01d18-108">EXAMPLES</span></span>

### <span data-ttu-id="01d18-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01d18-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="01d18-110">Tworzy nowy obszar nazw przekazywania w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="01d18-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="01d18-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01d18-111">PARAMETERS</span></span>

### <span data-ttu-id="01d18-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d18-112">-DefaultProfile</span></span>
<span data-ttu-id="01d18-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01d18-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01d18-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="01d18-114">-Location</span></span>
<span data-ttu-id="01d18-115">Lokalizacja obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="01d18-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="01d18-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01d18-116">-Name</span></span>
<span data-ttu-id="01d18-117">Nazwa obszaru nazw przekaźnika</span><span class="sxs-lookup"><span data-stu-id="01d18-117">Relay Namespace Name</span></span>

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

### <span data-ttu-id="01d18-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d18-118">-ResourceGroupName</span></span>
<span data-ttu-id="01d18-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="01d18-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="01d18-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="01d18-120">-Tag</span></span>
<span data-ttu-id="01d18-121">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="01d18-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="01d18-122">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="01d18-122">For example:</span></span>

<span data-ttu-id="01d18-123">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="01d18-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="01d18-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01d18-124">-Confirm</span></span>
<span data-ttu-id="01d18-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d18-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d18-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d18-126">-WhatIf</span></span>
<span data-ttu-id="01d18-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d18-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01d18-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01d18-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d18-129">CommonParameters</span></span>
<span data-ttu-id="01d18-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d18-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d18-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d18-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01d18-132">INPUTS</span></span>

### <span data-ttu-id="01d18-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d18-133">-ResourceGroupName</span></span>
 <span data-ttu-id="01d18-134">System. String</span><span class="sxs-lookup"><span data-stu-id="01d18-134">System.String</span></span>

### <span data-ttu-id="01d18-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="01d18-135">-NamespaceName</span></span>
 <span data-ttu-id="01d18-136">System. String</span><span class="sxs-lookup"><span data-stu-id="01d18-136">System.String</span></span>

### <span data-ttu-id="01d18-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="01d18-137">-Location</span></span>
 <span data-ttu-id="01d18-138">System. String</span><span class="sxs-lookup"><span data-stu-id="01d18-138">System.String</span></span>

### <span data-ttu-id="01d18-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="01d18-139">-SkuName</span></span>
 <span data-ttu-id="01d18-140">System. String</span><span class="sxs-lookup"><span data-stu-id="01d18-140">System.String</span></span>

### <span data-ttu-id="01d18-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="01d18-141">-Tag</span></span>
 <span data-ttu-id="01d18-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="01d18-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01d18-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01d18-143">OUTPUTS</span></span>

### <span data-ttu-id="01d18-144">Microsoft. Azure. Commands. Relay. modele. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="01d18-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="01d18-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01d18-145">NOTES</span></span>

## <span data-ttu-id="01d18-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01d18-146">RELATED LINKS</span></span>

