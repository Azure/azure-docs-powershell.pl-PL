---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896018"
---
# <span data-ttu-id="a3f0b-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a3f0b-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="a3f0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f0b-103">Tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="a3f0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3f0b-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3f0b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f0b-106">Polecenie cmdlet **New-AzRelayNamespace** tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="a3f0b-107">Po utworzeniu manifest zasobów przestrzeni nazw jest niezmienny.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="a3f0b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3f0b-108">EXAMPLES</span></span>

### <span data-ttu-id="a3f0b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3f0b-109">Example 1</span></span>
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

<span data-ttu-id="a3f0b-110">Tworzy nowy obszar nazw przekazywania w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="a3f0b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3f0b-111">PARAMETERS</span></span>

### <span data-ttu-id="a3f0b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f0b-112">-DefaultProfile</span></span>
<span data-ttu-id="a3f0b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3f0b-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a3f0b-114">-Location</span></span>
<span data-ttu-id="a3f0b-115">Lokalizacja obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="a3f0b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3f0b-116">-Name</span></span>
<span data-ttu-id="a3f0b-117">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a3f0b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f0b-118">-ResourceGroupName</span></span>
<span data-ttu-id="a3f0b-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="a3f0b-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3f0b-120">-Tag</span></span>
<span data-ttu-id="a3f0b-121">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="a3f0b-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3f0b-122">-Confirm</span></span>
<span data-ttu-id="a3f0b-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3f0b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3f0b-124">-WhatIf</span></span>
<span data-ttu-id="a3f0b-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3f0b-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3f0b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f0b-127">CommonParameters</span></span>
<span data-ttu-id="a3f0b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f0b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f0b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f0b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f0b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3f0b-130">INPUTS</span></span>

### <span data-ttu-id="a3f0b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a3f0b-131">System.String</span></span>

### <span data-ttu-id="a3f0b-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a3f0b-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a3f0b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3f0b-133">OUTPUTS</span></span>

### <span data-ttu-id="a3f0b-134">Microsoft. Azure. Commands. Relay. modele. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a3f0b-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="a3f0b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3f0b-135">NOTES</span></span>

## <span data-ttu-id="a3f0b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3f0b-136">RELATED LINKS</span></span>
