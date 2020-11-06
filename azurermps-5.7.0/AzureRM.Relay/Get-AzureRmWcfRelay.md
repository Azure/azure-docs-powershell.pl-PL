---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551655"
---
# <span data-ttu-id="7ea32-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="7ea32-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="7ea32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ea32-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea32-103">Zwraca opis określonego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="7ea32-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ea32-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea32-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ea32-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea32-106">Polecenie cmdlet **Get-AzureRmWcfRelay** zwraca opis określonego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="7ea32-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="7ea32-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ea32-107">EXAMPLES</span></span>

### <span data-ttu-id="7ea32-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ea32-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="7ea32-109">Zwraca opis WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="7ea32-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="7ea32-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ea32-110">PARAMETERS</span></span>

### <span data-ttu-id="7ea32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea32-111">-DefaultProfile</span></span>
<span data-ttu-id="7ea32-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea32-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ea32-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ea32-113">-Name</span></span>
<span data-ttu-id="7ea32-114">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="7ea32-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea32-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7ea32-115">-Namespace</span></span>
<span data-ttu-id="7ea32-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7ea32-116">Namespace Name.</span></span>

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

### <span data-ttu-id="7ea32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea32-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ea32-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ea32-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="7ea32-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea32-119">CommonParameters</span></span>
<span data-ttu-id="7ea32-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea32-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea32-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea32-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea32-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ea32-122">INPUTS</span></span>

### <span data-ttu-id="7ea32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea32-123">-ResourceGroupName</span></span>
 <span data-ttu-id="7ea32-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea32-124">System.String</span></span>
 

### <span data-ttu-id="7ea32-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7ea32-125">-Namespace</span></span>
 <span data-ttu-id="7ea32-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea32-126">System.String</span></span>
 

### <span data-ttu-id="7ea32-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ea32-127">-Name</span></span>
 <span data-ttu-id="7ea32-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea32-128">System.String</span></span> 

## <span data-ttu-id="7ea32-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ea32-129">OUTPUTS</span></span>

### <span data-ttu-id="7ea32-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. modele. WcfRelayAttributes, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="7ea32-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="7ea32-131">Relaytype: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: prawda RequiresTransportSecurity: prawda IsDynamic: false UserMetadata: Identyfikator meta danych użytkownika:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1</span><span class="sxs-lookup"><span data-stu-id="7ea32-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="7ea32-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ea32-132">NOTES</span></span>

## <span data-ttu-id="7ea32-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ea32-133">RELATED LINKS</span></span>

