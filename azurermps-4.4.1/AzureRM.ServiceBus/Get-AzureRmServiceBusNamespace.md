---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716664"
---
# <span data-ttu-id="c2549-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="c2549-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="c2549-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2549-102">SYNOPSIS</span></span>
<span data-ttu-id="c2549-103">Pobiera opis określonego obszaru nazw usługi Service Bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2549-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2549-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2549-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2549-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2549-105">DESCRIPTION</span></span>
<span data-ttu-id="c2549-106">Polecenie cmdlet **Get-AzureRmServiceBusNamespace** Pobiera opis określonego obszaru nazw usługi Service Bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2549-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="c2549-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2549-107">EXAMPLES</span></span>

### <span data-ttu-id="c2549-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2549-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="c2549-109">Zwraca opis określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c2549-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c2549-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2549-110">PARAMETERS</span></span>

### <span data-ttu-id="c2549-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2549-111">-DefaultProfile</span></span>
<span data-ttu-id="c2549-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2549-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2549-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2549-113">-Name</span></span>
<span data-ttu-id="c2549-114">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="c2549-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2549-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2549-115">-ResourceGroupName</span></span>
<span data-ttu-id="c2549-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c2549-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2549-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2549-117">CommonParameters</span></span>
<span data-ttu-id="c2549-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2549-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2549-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2549-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2549-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2549-120">INPUTS</span></span>

### <span data-ttu-id="c2549-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c2549-121">-ResourceGroup</span></span>
<span data-ttu-id="c2549-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c2549-122">System.String</span></span>

### <span data-ttu-id="c2549-123">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c2549-123">-NamespaceName</span></span>
 <span data-ttu-id="c2549-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c2549-124">System.String</span></span>

## <span data-ttu-id="c2549-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2549-125">OUTPUTS</span></span>

### <span data-ttu-id="c2549-126">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. NamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c2549-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c2549-127">Nazwa: SB-Example1 identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1: lokalizacja w zachodniej Stanach Zjednoczonych: Nazwa: Standard, Pojemność: 1, warstwa: standardowa ProvisioningState: stan pomyślny: Active CreatedAt: 1/20/2017 1:40:01 AM UpdatedAt: 1/20/2017 1:40:24 AM ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ Enabled: true</span><span class="sxs-lookup"><span data-stu-id="c2549-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="c2549-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2549-128">NOTES</span></span>
## <span data-ttu-id="c2549-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2549-129">RELATED LINKS</span></span>

## <span data-ttu-id="c2549-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2549-130">RELATED LINKS</span></span>

