---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 2fccb11ba45fa1d532c35140db588294895c0802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543036"
---
# <span data-ttu-id="426dd-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="426dd-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="426dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="426dd-102">SYNOPSIS</span></span>
<span data-ttu-id="426dd-103">Pobiera opis określonego HybridConnection w obszarze nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="426dd-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="426dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="426dd-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="426dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="426dd-105">DESCRIPTION</span></span>
<span data-ttu-id="426dd-106">Polecenie cmdlet **Get-AzureRmRelayHybridConnection** Pobiera opis określonego HybridConnection w obszarze nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="426dd-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="426dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="426dd-107">EXAMPLES</span></span>

### <span data-ttu-id="426dd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="426dd-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="426dd-109">Zwraca opis HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="426dd-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="426dd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="426dd-110">PARAMETERS</span></span>

### <span data-ttu-id="426dd-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="426dd-111">-Name</span></span>
<span data-ttu-id="426dd-112">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="426dd-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="426dd-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="426dd-113">-Namespace</span></span>
<span data-ttu-id="426dd-114">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="426dd-114">Namespace Name.</span></span>

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

### <span data-ttu-id="426dd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="426dd-115">-ResourceGroupName</span></span>
<span data-ttu-id="426dd-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="426dd-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="426dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426dd-117">-DefaultProfile</span></span>
<span data-ttu-id="426dd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="426dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426dd-119">CommonParameters</span></span>
<span data-ttu-id="426dd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="426dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426dd-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426dd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426dd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="426dd-122">INPUTS</span></span>

### <span data-ttu-id="426dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="426dd-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="426dd-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="426dd-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="426dd-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="426dd-125">-Name</span></span>
    System.String

## <span data-ttu-id="426dd-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="426dd-126">OUTPUTS</span></span>

### <span data-ttu-id="426dd-127">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. modele. HybridConnectionAttibutes, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="426dd-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="426dd-128">CreatedAt: 4/12/2017 3:17:02 AM UpdatedAt: 4/12/2017 3:17:02 AM ListenerCount: 0 RequiresClientAuthorization: true UserMetadata: Identyfikator meta danych użytkownika:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name: TestHybridConnection Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="426dd-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="426dd-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="426dd-129">NOTES</span></span>

## <span data-ttu-id="426dd-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="426dd-130">RELATED LINKS</span></span>

