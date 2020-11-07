---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709775"
---
# <span data-ttu-id="ed992-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ed992-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="ed992-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed992-102">SYNOPSIS</span></span>
<span data-ttu-id="ed992-103">Umożliwia zaktualizowanie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ed992-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ed992-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed992-104">SYNTAX</span></span>

### <span data-ttu-id="ed992-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed992-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed992-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed992-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed992-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ed992-107">DESCRIPTION</span></span>
<span data-ttu-id="ed992-108">Polecenie cmdlet Set-AzEventHubNamespace aktualizuje właściwości określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ed992-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ed992-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed992-109">EXAMPLES</span></span>

### <span data-ttu-id="ed992-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed992-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="ed992-111">Umożliwia zaktualizowanie stanu obszaru nazw NamespaceName \` \` .</span><span class="sxs-lookup"><span data-stu-id="ed992-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="ed992-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ed992-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="ed992-113">Umożliwia zaktualizowanie stanu przestrzeni nazw obszar_nazwname \` \` za pomocą funkcji autorozdęcie = włączone i MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="ed992-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="ed992-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed992-114">PARAMETERS</span></span>

### <span data-ttu-id="ed992-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed992-115">-DefaultProfile</span></span>
<span data-ttu-id="ed992-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed992-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed992-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="ed992-117">-EnableAutoInflate</span></span>
<span data-ttu-id="ed992-118">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="ed992-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ed992-119">-Location</span></span>
<span data-ttu-id="ed992-120">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="ed992-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="ed992-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="ed992-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="ed992-122">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="ed992-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed992-123">-Name</span></span>
<span data-ttu-id="ed992-124">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="ed992-124">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed992-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed992-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed992-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="ed992-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ed992-127">-SkuCapacity</span></span>
<span data-ttu-id="ed992-128">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="ed992-128">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ed992-129">-SkuName</span></span>
<span data-ttu-id="ed992-130">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="ed992-130">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-131">-State</span><span class="sxs-lookup"><span data-stu-id="ed992-131">-State</span></span>
<span data-ttu-id="ed992-132">Wyłącz/Włącz obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="ed992-132">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed992-133">-Tag</span></span>
<span data-ttu-id="ed992-134">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="ed992-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed992-135">-Confirm</span></span>
<span data-ttu-id="ed992-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed992-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed992-137">-WhatIf</span></span>
<span data-ttu-id="ed992-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed992-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed992-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ed992-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed992-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed992-140">CommonParameters</span></span>
<span data-ttu-id="ed992-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed992-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed992-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed992-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed992-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed992-143">INPUTS</span></span>

### <span data-ttu-id="ed992-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ed992-144">System.String</span></span>

### <span data-ttu-id="ed992-145">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ed992-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ed992-146">System. Nullable "1 [[Microsoft. Azure. Commands. EventHub. MODELES. NamespaceState; Microsoft. Azure. PowerShell. PowerShell. w wersji = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ed992-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ed992-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ed992-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ed992-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed992-148">OUTPUTS</span></span>

### <span data-ttu-id="ed992-149">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ed992-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ed992-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed992-150">NOTES</span></span>

## <span data-ttu-id="ed992-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed992-151">RELATED LINKS</span></span>
