---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 1e4e1d50df44715fe433a5106619264063b2f22e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708167"
---
# <span data-ttu-id="bb60d-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bb60d-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="bb60d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb60d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb60d-103">Pobiera opis określonego obszaru nazw usługi Service Bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb60d-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="bb60d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb60d-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb60d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb60d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb60d-106">Polecenie cmdlet **Get-AzServiceBusNamespace** Pobiera opis określonego obszaru nazw usługi Service Bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb60d-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="bb60d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb60d-107">EXAMPLES</span></span>

### <span data-ttu-id="bb60d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb60d-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="bb60d-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb60d-109">PARAMETERS</span></span>

### <span data-ttu-id="bb60d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb60d-110">-DefaultProfile</span></span>
<span data-ttu-id="bb60d-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb60d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb60d-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb60d-112">-Name</span></span>
<span data-ttu-id="bb60d-113">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="bb60d-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb60d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb60d-114">-ResourceGroupName</span></span>
<span data-ttu-id="bb60d-115">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bb60d-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb60d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb60d-116">CommonParameters</span></span>
<span data-ttu-id="bb60d-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb60d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb60d-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb60d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb60d-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb60d-119">INPUTS</span></span>

### <span data-ttu-id="bb60d-120">System. String</span><span class="sxs-lookup"><span data-stu-id="bb60d-120">System.String</span></span>

## <span data-ttu-id="bb60d-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb60d-121">OUTPUTS</span></span>

### <span data-ttu-id="bb60d-122">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bb60d-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="bb60d-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb60d-123">NOTES</span></span>

## <span data-ttu-id="bb60d-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb60d-124">RELATED LINKS</span></span>