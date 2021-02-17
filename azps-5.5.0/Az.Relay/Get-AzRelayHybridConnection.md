---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198762"
---
# <span data-ttu-id="ae699-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="ae699-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="ae699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae699-102">SYNOPSIS</span></span>
<span data-ttu-id="ae699-103">Pobiera opis określonego połączenia hybrydowego w przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="ae699-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="ae699-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae699-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae699-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae699-105">DESCRIPTION</span></span>
<span data-ttu-id="ae699-106">Polecenie **cmdlet Get-AzRelayHybridConnection** otrzymuje opis określonego połączenia hybrydowego w przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="ae699-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="ae699-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae699-107">EXAMPLES</span></span>

### <span data-ttu-id="ae699-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae699-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="ae699-109">Zwraca opis połączenia hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="ae699-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="ae699-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae699-110">PARAMETERS</span></span>

### <span data-ttu-id="ae699-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae699-111">-DefaultProfile</span></span>
<span data-ttu-id="ae699-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae699-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae699-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae699-113">-Name</span></span>
<span data-ttu-id="ae699-114">Nazwa usługi HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="ae699-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-115">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="ae699-115">-Namespace</span></span>
<span data-ttu-id="ae699-116">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ae699-116">Namespace Name.</span></span>

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

### <span data-ttu-id="ae699-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae699-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae699-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae699-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae699-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae699-119">CommonParameters</span></span>
<span data-ttu-id="ae699-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae699-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae699-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae699-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae699-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae699-122">INPUTS</span></span>

### <span data-ttu-id="ae699-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ae699-123">System.String</span></span>

## <span data-ttu-id="ae699-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae699-124">OUTPUTS</span></span>

### <span data-ttu-id="ae699-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="ae699-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="ae699-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae699-126">NOTES</span></span>

## <span data-ttu-id="ae699-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae699-127">RELATED LINKS</span></span>
