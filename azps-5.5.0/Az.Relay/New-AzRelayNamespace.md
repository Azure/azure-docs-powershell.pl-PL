---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242658"
---
# <span data-ttu-id="94b84-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="94b84-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="94b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94b84-102">SYNOPSIS</span></span>
<span data-ttu-id="94b84-103">Tworzy nową przestrzeń nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="94b84-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="94b84-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94b84-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94b84-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="94b84-105">DESCRIPTION</span></span>
<span data-ttu-id="94b84-106">Polecenie **cmdlet New-AzRelayNamespace** tworzy nową przestrzeń nazw relay.</span><span class="sxs-lookup"><span data-stu-id="94b84-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="94b84-107">Po utworzeniu manifestu zasobu przestrzeni nazw jest nieumiejętny.</span><span class="sxs-lookup"><span data-stu-id="94b84-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="94b84-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94b84-108">EXAMPLES</span></span>

### <span data-ttu-id="94b84-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94b84-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="94b84-110">Tworzy nową przestrzeń nazw Przekazywanie w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94b84-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="94b84-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94b84-111">PARAMETERS</span></span>

### <span data-ttu-id="94b84-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b84-112">-DefaultProfile</span></span>
<span data-ttu-id="94b84-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94b84-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94b84-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="94b84-114">-Location</span></span>
<span data-ttu-id="94b84-115">Lokalizacja przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="94b84-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="94b84-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94b84-116">-Name</span></span>
<span data-ttu-id="94b84-117">Nazwa przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="94b84-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="94b84-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b84-118">-ResourceGroupName</span></span>
<span data-ttu-id="94b84-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94b84-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="94b84-120">— Tag</span><span class="sxs-lookup"><span data-stu-id="94b84-120">-Tag</span></span>
<span data-ttu-id="94b84-121">Skróty reprezentujące tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="94b84-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="94b84-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94b84-122">-Confirm</span></span>
<span data-ttu-id="94b84-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94b84-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b84-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b84-124">-WhatIf</span></span>
<span data-ttu-id="94b84-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94b84-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94b84-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94b84-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b84-127">CommonParameters</span></span>
<span data-ttu-id="94b84-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b84-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b84-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b84-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94b84-130">INPUTS</span></span>

### <span data-ttu-id="94b84-131">System.String</span><span class="sxs-lookup"><span data-stu-id="94b84-131">System.String</span></span>

### <span data-ttu-id="94b84-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="94b84-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94b84-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94b84-133">OUTPUTS</span></span>

### <span data-ttu-id="94b84-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="94b84-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="94b84-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94b84-135">NOTES</span></span>

## <span data-ttu-id="94b84-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94b84-136">RELATED LINKS</span></span>
