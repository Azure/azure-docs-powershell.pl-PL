---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: ef4d7ccf2f56d8a6d2a70fa4efb9468365cfcd32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993420"
---
# <span data-ttu-id="d3a3e-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d3a3e-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="d3a3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a3e-103">Pobiera opis dla określonej przestrzeni nazw typu service bus w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3a3e-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="d3a3e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3a3e-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3a3e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a3e-106">Polecenie **cmdlet Get-AzServiceBusNamespace** pobiera opis określonej przestrzeni nazw typu bus usługi w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3a3e-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="d3a3e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3a3e-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a3e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3a3e-108">Example 1</span></span>

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

## <span data-ttu-id="d3a3e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a3e-109">PARAMETERS</span></span>

### <span data-ttu-id="d3a3e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a3e-110">-DefaultProfile</span></span>
<span data-ttu-id="d3a3e-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a3e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3a3e-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d3a3e-112">-Name</span></span>
<span data-ttu-id="d3a3e-113">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d3a3e-113">Namespace Name.</span></span>

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

### <span data-ttu-id="d3a3e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a3e-114">-ResourceGroupName</span></span>
<span data-ttu-id="d3a3e-115">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d3a3e-115">The name of the resource group</span></span>

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

### <span data-ttu-id="d3a3e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a3e-116">CommonParameters</span></span>
<span data-ttu-id="d3a3e-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a3e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a3e-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a3e-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a3e-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3a3e-119">INPUTS</span></span>

### <span data-ttu-id="d3a3e-120">System.String</span><span class="sxs-lookup"><span data-stu-id="d3a3e-120">System.String</span></span>

## <span data-ttu-id="d3a3e-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3a3e-121">OUTPUTS</span></span>

### <span data-ttu-id="d3a3e-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d3a3e-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d3a3e-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3a3e-123">NOTES</span></span>

## <span data-ttu-id="d3a3e-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3a3e-124">RELATED LINKS</span></span>
