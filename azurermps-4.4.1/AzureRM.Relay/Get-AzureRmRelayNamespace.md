---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: 5f1e8037e4a9faef508c2ffd62ff00aca4387cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543035"
---
# <span data-ttu-id="86510-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="86510-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="86510-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86510-102">SYNOPSIS</span></span>
<span data-ttu-id="86510-103">Pobiera opis określonego obszaru nazw przekaźnika w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="86510-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86510-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86510-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86510-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86510-105">DESCRIPTION</span></span>
<span data-ttu-id="86510-106">Polecenie cmdlet **Get-AzureRmRelayNamespace** Pobiera opis określonego obszaru nazw przekaźnika w obrębie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86510-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="86510-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86510-107">EXAMPLES</span></span>

### <span data-ttu-id="86510-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86510-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="86510-109">Zwraca opis określonego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="86510-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="86510-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86510-110">PARAMETERS</span></span>

### <span data-ttu-id="86510-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86510-111">-Name</span></span>
<span data-ttu-id="86510-112">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="86510-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="86510-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86510-113">-ResourceGroupName</span></span>
<span data-ttu-id="86510-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86510-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="86510-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86510-115">-DefaultProfile</span></span>
<span data-ttu-id="86510-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86510-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86510-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86510-117">CommonParameters</span></span>
<span data-ttu-id="86510-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86510-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86510-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86510-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86510-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86510-120">INPUTS</span></span>

### <span data-ttu-id="86510-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86510-121">-ResourceGroupName</span></span>
<span data-ttu-id="86510-122">System. String</span><span class="sxs-lookup"><span data-stu-id="86510-122">System.String</span></span>

### <span data-ttu-id="86510-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86510-123">-Name</span></span>
 <span data-ttu-id="86510-124">System. String</span><span class="sxs-lookup"><span data-stu-id="86510-124">System.String</span></span>

## <span data-ttu-id="86510-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86510-125">OUTPUTS</span></span>

### <span data-ttu-id="86510-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. modele. RelayNamespaceAttributes, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="86510-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="86510-127">ProvisioningState: powiodło się CreatedAt: 4/12/2017 12:38:47 AM UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428F-8f3c-f2affa9b2f7d: TestNamespace-Relay1 Location: zachodnie znaczniki w Stanach Zjednoczonych: {[tag1, Tag1Value]} ID:/subscriptions/854d368f-1828-428F-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1 Name: TestNameSpace-Relay1 Type: Microsoft. Relay/obszary nazw</span><span class="sxs-lookup"><span data-stu-id="86510-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="86510-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86510-128">NOTES</span></span>

## <span data-ttu-id="86510-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86510-129">RELATED LINKS</span></span>

