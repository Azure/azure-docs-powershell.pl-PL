---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 359ff0ce6de0c017d1ea2a65adc1d4573e45c17f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191170"
---
# <span data-ttu-id="417e0-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="417e0-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="417e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="417e0-102">SYNOPSIS</span></span>
<span data-ttu-id="417e0-103">Pobiera opis dla określonej przestrzeni nazw typu service bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="417e0-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="417e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="417e0-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="417e0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="417e0-105">DESCRIPTION</span></span>
<span data-ttu-id="417e0-106">Polecenie **cmdlet Get-AzServiceBusNamespace** pobiera opis określonej przestrzeni nazw typu Bus usługi w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="417e0-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="417e0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="417e0-107">EXAMPLES</span></span>

### <span data-ttu-id="417e0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="417e0-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="417e0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="417e0-109">PARAMETERS</span></span>

### <span data-ttu-id="417e0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417e0-110">-DefaultProfile</span></span>
<span data-ttu-id="417e0-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="417e0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="417e0-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="417e0-112">-Name</span></span>
<span data-ttu-id="417e0-113">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="417e0-113">Namespace Name.</span></span>

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

### <span data-ttu-id="417e0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="417e0-114">-ResourceGroupName</span></span>
<span data-ttu-id="417e0-115">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="417e0-115">The name of the resource group</span></span>

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

### <span data-ttu-id="417e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417e0-116">CommonParameters</span></span>
<span data-ttu-id="417e0-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="417e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417e0-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="417e0-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417e0-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="417e0-119">INPUTS</span></span>

### <span data-ttu-id="417e0-120">System.String</span><span class="sxs-lookup"><span data-stu-id="417e0-120">System.String</span></span>

## <span data-ttu-id="417e0-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="417e0-121">OUTPUTS</span></span>

### <span data-ttu-id="417e0-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="417e0-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="417e0-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="417e0-123">NOTES</span></span>

## <span data-ttu-id="417e0-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="417e0-124">RELATED LINKS</span></span>
