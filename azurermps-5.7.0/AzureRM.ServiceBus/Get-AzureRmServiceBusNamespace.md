---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2584630c8c1d0981f354ffc920af4f8ed9ff979f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542283"
---
# <span data-ttu-id="54f50-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="54f50-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="54f50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54f50-102">SYNOPSIS</span></span>
<span data-ttu-id="54f50-103">Pobiera opis określonego obszaru nazw usługi Service Bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="54f50-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54f50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54f50-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54f50-105">Opis</span><span class="sxs-lookup"><span data-stu-id="54f50-105">DESCRIPTION</span></span>
<span data-ttu-id="54f50-106">Polecenie cmdlet **Get-AzureRmServiceBusNamespace** Pobiera opis określonego obszaru nazw usługi Service Bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="54f50-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="54f50-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54f50-107">EXAMPLES</span></span>

### <span data-ttu-id="54f50-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="54f50-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/

```

## <span data-ttu-id="54f50-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54f50-109">PARAMETERS</span></span>

### <span data-ttu-id="54f50-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f50-110">-DefaultProfile</span></span>
<span data-ttu-id="54f50-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54f50-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54f50-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54f50-112">-Name</span></span>
<span data-ttu-id="54f50-113">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="54f50-113">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f50-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f50-114">-ResourceGroupName</span></span>
<span data-ttu-id="54f50-115">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="54f50-115">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f50-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f50-116">CommonParameters</span></span>
<span data-ttu-id="54f50-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f50-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f50-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f50-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f50-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54f50-119">INPUTS</span></span>

### <span data-ttu-id="54f50-120">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="54f50-120">-ResourceGroup</span></span>
<span data-ttu-id="54f50-121">System. String</span><span class="sxs-lookup"><span data-stu-id="54f50-121">System.String</span></span>

### <span data-ttu-id="54f50-122">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="54f50-122">-NamespaceName</span></span>
 <span data-ttu-id="54f50-123">System. String</span><span class="sxs-lookup"><span data-stu-id="54f50-123">System.String</span></span>

## <span data-ttu-id="54f50-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54f50-124">OUTPUTS</span></span>

### <span data-ttu-id="54f50-125">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. PSNamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="54f50-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54f50-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54f50-126">NOTES</span></span>

## <span data-ttu-id="54f50-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54f50-127">RELATED LINKS</span></span>

