---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490665"
---
# <span data-ttu-id="02eec-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="02eec-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="02eec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02eec-102">SYNOPSIS</span></span>
<span data-ttu-id="02eec-103">Pobiera opis określonego HybridConnection w obszarze nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="02eec-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="02eec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02eec-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02eec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02eec-105">DESCRIPTION</span></span>
<span data-ttu-id="02eec-106">Polecenie cmdlet **Get-AzRelayHybridConnection** Pobiera opis określonego HybridConnection w obszarze nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="02eec-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="02eec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02eec-107">EXAMPLES</span></span>

### <span data-ttu-id="02eec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02eec-108">Example 1</span></span>
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

<span data-ttu-id="02eec-109">Zwraca opis HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="02eec-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="02eec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02eec-110">PARAMETERS</span></span>

### <span data-ttu-id="02eec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02eec-111">-DefaultProfile</span></span>
<span data-ttu-id="02eec-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02eec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02eec-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02eec-113">-Name</span></span>
<span data-ttu-id="02eec-114">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="02eec-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="02eec-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="02eec-115">-Namespace</span></span>
<span data-ttu-id="02eec-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="02eec-116">Namespace Name.</span></span>

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

### <span data-ttu-id="02eec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02eec-117">-ResourceGroupName</span></span>
<span data-ttu-id="02eec-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02eec-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="02eec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02eec-119">CommonParameters</span></span>
<span data-ttu-id="02eec-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02eec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02eec-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02eec-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02eec-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02eec-122">INPUTS</span></span>

### <span data-ttu-id="02eec-123">System. String</span><span class="sxs-lookup"><span data-stu-id="02eec-123">System.String</span></span>

## <span data-ttu-id="02eec-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02eec-124">OUTPUTS</span></span>

### <span data-ttu-id="02eec-125">Microsoft. Azure. Commands. Relay. modele. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="02eec-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="02eec-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02eec-126">NOTES</span></span>

## <span data-ttu-id="02eec-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02eec-127">RELATED LINKS</span></span>
