---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240147"
---
# <span data-ttu-id="25fb8-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="25fb8-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="25fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="25fb8-103">Pobiera opis określonej przestrzeni nazw przekazywania w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="25fb8-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="25fb8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25fb8-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25fb8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="25fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="25fb8-106">Polecenie **cmdlet Get-AzRelayNamespace** pobiera opis określonej przestrzeni nazw Relay w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="25fb8-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="25fb8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25fb8-107">EXAMPLES</span></span>

### <span data-ttu-id="25fb8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25fb8-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="25fb8-109">Zwraca opis określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="25fb8-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="25fb8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25fb8-110">PARAMETERS</span></span>

### <span data-ttu-id="25fb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fb8-111">-DefaultProfile</span></span>
<span data-ttu-id="25fb8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25fb8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25fb8-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25fb8-113">-Name</span></span>
<span data-ttu-id="25fb8-114">Nazwa przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="25fb8-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25fb8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25fb8-115">-ResourceGroupName</span></span>
<span data-ttu-id="25fb8-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25fb8-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25fb8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fb8-117">CommonParameters</span></span>
<span data-ttu-id="25fb8-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25fb8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fb8-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25fb8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fb8-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25fb8-120">INPUTS</span></span>

### <span data-ttu-id="25fb8-121">System.String</span><span class="sxs-lookup"><span data-stu-id="25fb8-121">System.String</span></span>

## <span data-ttu-id="25fb8-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25fb8-122">OUTPUTS</span></span>

### <span data-ttu-id="25fb8-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="25fb8-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="25fb8-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25fb8-124">NOTES</span></span>

## <span data-ttu-id="25fb8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25fb8-125">RELATED LINKS</span></span>
