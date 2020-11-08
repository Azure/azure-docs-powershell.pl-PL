---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063245"
---
# <span data-ttu-id="52002-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="52002-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="52002-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52002-102">SYNOPSIS</span></span>
<span data-ttu-id="52002-103">Zwraca opis określonego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="52002-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="52002-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52002-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52002-105">Opis</span><span class="sxs-lookup"><span data-stu-id="52002-105">DESCRIPTION</span></span>
<span data-ttu-id="52002-106">Polecenie cmdlet **Get-AzWcfRelay** zwraca opis określonego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="52002-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="52002-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52002-107">EXAMPLES</span></span>

### <span data-ttu-id="52002-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="52002-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="52002-109">Zwraca opis WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="52002-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="52002-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52002-110">PARAMETERS</span></span>

### <span data-ttu-id="52002-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52002-111">-DefaultProfile</span></span>
<span data-ttu-id="52002-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="52002-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52002-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="52002-113">-Name</span></span>
<span data-ttu-id="52002-114">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="52002-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52002-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="52002-115">-Namespace</span></span>
<span data-ttu-id="52002-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="52002-116">Namespace Name.</span></span>

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

### <span data-ttu-id="52002-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52002-117">-ResourceGroupName</span></span>
<span data-ttu-id="52002-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="52002-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="52002-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52002-119">CommonParameters</span></span>
<span data-ttu-id="52002-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52002-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52002-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52002-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52002-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52002-122">INPUTS</span></span>

### <span data-ttu-id="52002-123">System. String</span><span class="sxs-lookup"><span data-stu-id="52002-123">System.String</span></span>

## <span data-ttu-id="52002-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52002-124">OUTPUTS</span></span>

### <span data-ttu-id="52002-125">Microsoft. Azure. Commands. Relay. modele. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="52002-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="52002-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52002-126">NOTES</span></span>

## <span data-ttu-id="52002-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52002-127">RELATED LINKS</span></span>
