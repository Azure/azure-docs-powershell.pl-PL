---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: 37e641516ffc21a0984f97cb84f94d2564033fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708470"
---
# <span data-ttu-id="f7141-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="f7141-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="f7141-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7141-102">SYNOPSIS</span></span>
<span data-ttu-id="f7141-103">Tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="f7141-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="f7141-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7141-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7141-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7141-105">DESCRIPTION</span></span>
<span data-ttu-id="f7141-106">Polecenie cmdlet **New-AzRelayNamespace** tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="f7141-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="f7141-107">Po utworzeniu manifest zasobów przestrzeni nazw jest niezmienny.</span><span class="sxs-lookup"><span data-stu-id="f7141-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="f7141-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7141-108">EXAMPLES</span></span>

### <span data-ttu-id="f7141-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7141-109">Example 1</span></span>
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

<span data-ttu-id="f7141-110">Tworzy nowy obszar nazw przekazywania w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7141-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="f7141-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7141-111">PARAMETERS</span></span>

### <span data-ttu-id="f7141-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7141-112">-DefaultProfile</span></span>
<span data-ttu-id="f7141-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7141-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7141-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f7141-114">-Location</span></span>
<span data-ttu-id="f7141-115">Lokalizacja obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="f7141-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="f7141-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7141-116">-Name</span></span>
<span data-ttu-id="f7141-117">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="f7141-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="f7141-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7141-118">-ResourceGroupName</span></span>
<span data-ttu-id="f7141-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7141-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7141-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7141-120">-Tag</span></span>
<span data-ttu-id="f7141-121">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7141-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="f7141-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7141-122">-Confirm</span></span>
<span data-ttu-id="f7141-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7141-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7141-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7141-124">-WhatIf</span></span>
<span data-ttu-id="f7141-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7141-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7141-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7141-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7141-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7141-127">CommonParameters</span></span>
<span data-ttu-id="f7141-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7141-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7141-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7141-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7141-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7141-130">INPUTS</span></span>

### <span data-ttu-id="f7141-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f7141-131">System.String</span></span>

### <span data-ttu-id="f7141-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7141-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f7141-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7141-133">OUTPUTS</span></span>

### <span data-ttu-id="f7141-134">Microsoft. Azure. Commands. Relay. modele. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f7141-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="f7141-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7141-135">NOTES</span></span>

## <span data-ttu-id="f7141-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7141-136">RELATED LINKS</span></span>