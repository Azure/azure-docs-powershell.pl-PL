---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 546dbdfe2de2a87c0ce2887c83139a527ecf769c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708474"
---
# <span data-ttu-id="6a9b2-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="6a9b2-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="6a9b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9b2-103">Zwraca opis określonego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="6a9b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a9b2-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a9b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a9b2-105">DESCRIPTION</span></span>
<span data-ttu-id="6a9b2-106">Polecenie cmdlet **Get-AzWcfRelay** zwraca opis określonego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="6a9b2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a9b2-107">EXAMPLES</span></span>

### <span data-ttu-id="6a9b2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6a9b2-108">Example 1</span></span>
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

<span data-ttu-id="6a9b2-109">Zwraca opis WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="6a9b2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a9b2-110">PARAMETERS</span></span>

### <span data-ttu-id="6a9b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9b2-111">-DefaultProfile</span></span>
<span data-ttu-id="6a9b2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a9b2-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a9b2-113">-Name</span></span>
<span data-ttu-id="6a9b2-114">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6a9b2-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a9b2-115">-Namespace</span></span>
<span data-ttu-id="6a9b2-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-116">Namespace Name.</span></span>

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

### <span data-ttu-id="6a9b2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9b2-117">-ResourceGroupName</span></span>
<span data-ttu-id="6a9b2-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="6a9b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9b2-119">CommonParameters</span></span>
<span data-ttu-id="6a9b2-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9b2-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9b2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9b2-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a9b2-122">INPUTS</span></span>

### <span data-ttu-id="6a9b2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6a9b2-123">System.String</span></span>

## <span data-ttu-id="6a9b2-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a9b2-124">OUTPUTS</span></span>

### <span data-ttu-id="6a9b2-125">Microsoft. Azure. Commands. Relay. modele. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="6a9b2-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="6a9b2-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a9b2-126">NOTES</span></span>

## <span data-ttu-id="6a9b2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a9b2-127">RELATED LINKS</span></span>
