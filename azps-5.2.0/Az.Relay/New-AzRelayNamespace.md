---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368053"
---
# <span data-ttu-id="1ec06-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="1ec06-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="1ec06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ec06-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec06-103">Tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="1ec06-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="1ec06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ec06-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ec06-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec06-106">Polecenie cmdlet **New-AzRelayNamespace** tworzy nowy obszar nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="1ec06-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="1ec06-107">Po utworzeniu manifest zasobów przestrzeni nazw jest niezmienny.</span><span class="sxs-lookup"><span data-stu-id="1ec06-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="1ec06-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ec06-108">EXAMPLES</span></span>

### <span data-ttu-id="1ec06-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ec06-109">Example 1</span></span>
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

<span data-ttu-id="1ec06-110">Tworzy nowy obszar nazw przekazywania w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ec06-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="1ec06-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ec06-111">PARAMETERS</span></span>

### <span data-ttu-id="1ec06-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec06-112">-DefaultProfile</span></span>
<span data-ttu-id="1ec06-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec06-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec06-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1ec06-114">-Location</span></span>
<span data-ttu-id="1ec06-115">Lokalizacja obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="1ec06-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="1ec06-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ec06-116">-Name</span></span>
<span data-ttu-id="1ec06-117">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="1ec06-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="1ec06-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec06-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ec06-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ec06-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="1ec06-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ec06-120">-Tag</span></span>
<span data-ttu-id="1ec06-121">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ec06-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="1ec06-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ec06-122">-Confirm</span></span>
<span data-ttu-id="1ec06-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec06-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec06-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec06-124">-WhatIf</span></span>
<span data-ttu-id="1ec06-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec06-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec06-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ec06-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec06-127">CommonParameters</span></span>
<span data-ttu-id="1ec06-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec06-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec06-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec06-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ec06-130">INPUTS</span></span>

### <span data-ttu-id="1ec06-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1ec06-131">System.String</span></span>

### <span data-ttu-id="1ec06-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ec06-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1ec06-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ec06-133">OUTPUTS</span></span>

### <span data-ttu-id="1ec06-134">Microsoft. Azure. Commands. Relay. modele. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1ec06-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="1ec06-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ec06-135">NOTES</span></span>

## <span data-ttu-id="1ec06-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ec06-136">RELATED LINKS</span></span>
