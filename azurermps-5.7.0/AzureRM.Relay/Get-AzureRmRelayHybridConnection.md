---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 08a20958975d78a945e3e73729d5841f6dda6811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549588"
---
# <span data-ttu-id="1149f-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="1149f-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="1149f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1149f-102">SYNOPSIS</span></span>
<span data-ttu-id="1149f-103">Pobiera opis określonego HybridConnection w obszarze nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="1149f-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1149f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1149f-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1149f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1149f-105">DESCRIPTION</span></span>
<span data-ttu-id="1149f-106">Polecenie cmdlet **Get-AzureRmRelayHybridConnection** Pobiera opis określonego HybridConnection w obszarze nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="1149f-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="1149f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1149f-107">EXAMPLES</span></span>

### <span data-ttu-id="1149f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1149f-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="1149f-109">Zwraca opis HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="1149f-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="1149f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1149f-110">PARAMETERS</span></span>

### <span data-ttu-id="1149f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1149f-111">-DefaultProfile</span></span>
<span data-ttu-id="1149f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1149f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1149f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1149f-113">-Name</span></span>
<span data-ttu-id="1149f-114">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="1149f-114">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1149f-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1149f-115">-Namespace</span></span>
<span data-ttu-id="1149f-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="1149f-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1149f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1149f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1149f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1149f-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1149f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1149f-119">CommonParameters</span></span>
<span data-ttu-id="1149f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1149f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1149f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1149f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1149f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1149f-122">INPUTS</span></span>

### <span data-ttu-id="1149f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1149f-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="1149f-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1149f-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="1149f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1149f-125">-Name</span></span>
    System.String

## <span data-ttu-id="1149f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1149f-126">OUTPUTS</span></span>

### <span data-ttu-id="1149f-127">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. modele. HybridConnectionAttibutes, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="1149f-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="1149f-128">CreatedAt: 4/12/2017 3:17:02 AM UpdatedAt: 4/12/2017 3:17:02 AM ListenerCount: 0 RequiresClientAuthorization: true UserMetadata: Identyfikator meta danych użytkownika:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name: TestHybridConnection Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="1149f-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="1149f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1149f-129">NOTES</span></span>

## <span data-ttu-id="1149f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1149f-130">RELATED LINKS</span></span>

