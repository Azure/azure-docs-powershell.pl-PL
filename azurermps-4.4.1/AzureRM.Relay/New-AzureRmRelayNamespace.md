---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 365a80e1ddf5673be5c45c5d17b24490c277a365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718106"
---
# <span data-ttu-id="569ee-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="569ee-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="569ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="569ee-102">SYNOPSIS</span></span>
<span data-ttu-id="569ee-103">Tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="569ee-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="569ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="569ee-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="569ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="569ee-105">DESCRIPTION</span></span>
<span data-ttu-id="569ee-106">Polecenie cmdlet **New-AzureRmRelayNamespace** tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="569ee-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="569ee-107">Po utworzeniu manifest zasobów przestrzeni nazw jest niezmienny.</span><span class="sxs-lookup"><span data-stu-id="569ee-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="569ee-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="569ee-108">EXAMPLES</span></span>

### <span data-ttu-id="569ee-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="569ee-109">Example 1</span></span>
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

<span data-ttu-id="569ee-110">Tworzy nowy obszar nazw przekazywania w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="569ee-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="569ee-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="569ee-111">PARAMETERS</span></span>

### <span data-ttu-id="569ee-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="569ee-112">-Location</span></span>
<span data-ttu-id="569ee-113">Lokalizacja obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="569ee-113">Relay Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569ee-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="569ee-114">-ResourceGroupName</span></span>
<span data-ttu-id="569ee-115">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="569ee-115">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569ee-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="569ee-116">-Tag</span></span>
<span data-ttu-id="569ee-117">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="569ee-117">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="569ee-118">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="569ee-118">For example:</span></span>

<span data-ttu-id="569ee-119">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="569ee-119">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="569ee-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="569ee-120">-Confirm</span></span>
<span data-ttu-id="569ee-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="569ee-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="569ee-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="569ee-122">-WhatIf</span></span>
<span data-ttu-id="569ee-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="569ee-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="569ee-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="569ee-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="569ee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569ee-125">-DefaultProfile</span></span>
<span data-ttu-id="569ee-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="569ee-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="569ee-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="569ee-127">-Name</span></span>
<span data-ttu-id="569ee-128">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="569ee-128">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569ee-129">CommonParameters</span></span>
<span data-ttu-id="569ee-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="569ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569ee-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="569ee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569ee-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="569ee-132">INPUTS</span></span>

### <span data-ttu-id="569ee-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="569ee-133">-ResourceGroupName</span></span>
 <span data-ttu-id="569ee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="569ee-134">System.String</span></span>

### <span data-ttu-id="569ee-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="569ee-135">-NamespaceName</span></span>
 <span data-ttu-id="569ee-136">System. String</span><span class="sxs-lookup"><span data-stu-id="569ee-136">System.String</span></span>

### <span data-ttu-id="569ee-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="569ee-137">-Location</span></span>
 <span data-ttu-id="569ee-138">System. String</span><span class="sxs-lookup"><span data-stu-id="569ee-138">System.String</span></span>

### <span data-ttu-id="569ee-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="569ee-139">-SkuName</span></span>
 <span data-ttu-id="569ee-140">System. String</span><span class="sxs-lookup"><span data-stu-id="569ee-140">System.String</span></span>

### <span data-ttu-id="569ee-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="569ee-141">-Tag</span></span>
 <span data-ttu-id="569ee-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="569ee-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="569ee-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="569ee-143">OUTPUTS</span></span>

### <span data-ttu-id="569ee-144">Microsoft. Azure. Commands. Relay. modele. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="569ee-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="569ee-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="569ee-145">NOTES</span></span>

## <span data-ttu-id="569ee-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="569ee-146">RELATED LINKS</span></span>

