---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: fe0991296ad5f2dc8be89c92117e74c4231b495c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718481"
---
# <span data-ttu-id="37e53-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="37e53-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="37e53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37e53-102">SYNOPSIS</span></span>
<span data-ttu-id="37e53-103">Pobiera opis określonego obszaru nazw przekaźnika w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="37e53-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37e53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37e53-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37e53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="37e53-105">DESCRIPTION</span></span>
<span data-ttu-id="37e53-106">Polecenie cmdlet **Get-AzureRmRelayNamespace** Pobiera opis określonego obszaru nazw przekaźnika w obrębie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37e53-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="37e53-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37e53-107">EXAMPLES</span></span>

### <span data-ttu-id="37e53-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37e53-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="37e53-109">Zwraca opis określonego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="37e53-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="37e53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37e53-110">PARAMETERS</span></span>

### <span data-ttu-id="37e53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e53-111">-DefaultProfile</span></span>
<span data-ttu-id="37e53-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37e53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37e53-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37e53-113">-Name</span></span>
<span data-ttu-id="37e53-114">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="37e53-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e53-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e53-115">-ResourceGroupName</span></span>
<span data-ttu-id="37e53-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37e53-116">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e53-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e53-117">CommonParameters</span></span>
<span data-ttu-id="37e53-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e53-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e53-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e53-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e53-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37e53-120">INPUTS</span></span>

### <span data-ttu-id="37e53-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e53-121">-ResourceGroupName</span></span>
<span data-ttu-id="37e53-122">System. String</span><span class="sxs-lookup"><span data-stu-id="37e53-122">System.String</span></span>

### <span data-ttu-id="37e53-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37e53-123">-Name</span></span>
 <span data-ttu-id="37e53-124">System. String</span><span class="sxs-lookup"><span data-stu-id="37e53-124">System.String</span></span>

## <span data-ttu-id="37e53-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37e53-125">OUTPUTS</span></span>

### <span data-ttu-id="37e53-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. modele. RelayNamespaceAttributes, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="37e53-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="37e53-127">ProvisioningState: powiodło się CreatedAt: 4/12/2017 12:38:47 AM UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428F-8f3c-f2affa9b2f7d: TestNamespace-Relay1 Location: zachodnie znaczniki w Stanach Zjednoczonych: {[tag1, Tag1Value]} ID:/subscriptions/854d368f-1828-428F-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1 Name: TestNameSpace-Relay1 Type: Microsoft. Relay/obszary nazw</span><span class="sxs-lookup"><span data-stu-id="37e53-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="37e53-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37e53-128">NOTES</span></span>

## <span data-ttu-id="37e53-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37e53-129">RELATED LINKS</span></span>

