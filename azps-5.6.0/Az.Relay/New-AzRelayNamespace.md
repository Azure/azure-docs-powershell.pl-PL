---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c6f0fc3d8a0ef96a8b54b954e07fb1a9d1c644e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000506"
---
# <span data-ttu-id="056b0-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="056b0-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="056b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="056b0-102">SYNOPSIS</span></span>
<span data-ttu-id="056b0-103">Tworzy nową przestrzeń nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="056b0-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="056b0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="056b0-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="056b0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="056b0-105">DESCRIPTION</span></span>
<span data-ttu-id="056b0-106">Polecenie **cmdlet New-AzRelayNamespace** tworzy nową przestrzeń nazw relay.</span><span class="sxs-lookup"><span data-stu-id="056b0-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="056b0-107">Po utworzeniu manifestu zasobu przestrzeni nazw jest nieumiejętny.</span><span class="sxs-lookup"><span data-stu-id="056b0-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="056b0-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="056b0-108">EXAMPLES</span></span>

### <span data-ttu-id="056b0-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="056b0-109">Example 1</span></span>
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

<span data-ttu-id="056b0-110">Tworzy nową przestrzeń nazw Przekazywanie w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="056b0-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="056b0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="056b0-111">PARAMETERS</span></span>

### <span data-ttu-id="056b0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="056b0-112">-DefaultProfile</span></span>
<span data-ttu-id="056b0-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="056b0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="056b0-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="056b0-114">-Location</span></span>
<span data-ttu-id="056b0-115">Lokalizacja przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="056b0-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="056b0-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="056b0-116">-Name</span></span>
<span data-ttu-id="056b0-117">Nazwa przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="056b0-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="056b0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="056b0-118">-ResourceGroupName</span></span>
<span data-ttu-id="056b0-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="056b0-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="056b0-120">— Tag</span><span class="sxs-lookup"><span data-stu-id="056b0-120">-Tag</span></span>
<span data-ttu-id="056b0-121">Skróty reprezentujące tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="056b0-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="056b0-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="056b0-122">-Confirm</span></span>
<span data-ttu-id="056b0-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="056b0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="056b0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="056b0-124">-WhatIf</span></span>
<span data-ttu-id="056b0-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="056b0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="056b0-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="056b0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="056b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="056b0-127">CommonParameters</span></span>
<span data-ttu-id="056b0-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="056b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="056b0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="056b0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="056b0-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="056b0-130">INPUTS</span></span>

### <span data-ttu-id="056b0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="056b0-131">System.String</span></span>

### <span data-ttu-id="056b0-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="056b0-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="056b0-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="056b0-133">OUTPUTS</span></span>

### <span data-ttu-id="056b0-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="056b0-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="056b0-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="056b0-135">NOTES</span></span>

## <span data-ttu-id="056b0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="056b0-136">RELATED LINKS</span></span>
