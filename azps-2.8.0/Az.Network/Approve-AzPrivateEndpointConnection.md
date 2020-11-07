---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9b47fb1954b13e28268f6b7aad66fa8190e20584
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870312"
---
# <span data-ttu-id="6c834-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6c834-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="6c834-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c834-102">SYNOPSIS</span></span>
<span data-ttu-id="6c834-103">Zatwierdza połączenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6c834-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="6c834-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c834-104">SYNTAX</span></span>

### <span data-ttu-id="6c834-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c834-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c834-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="6c834-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c834-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6c834-107">DESCRIPTION</span></span>
<span data-ttu-id="6c834-108">Polecenie cmdlet **zatwierdzanie — AzPrivateEndpointConnection** umożliwia zatwierdzenie prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6c834-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="6c834-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c834-109">EXAMPLES</span></span>

### <span data-ttu-id="6c834-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c834-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="6c834-111">W tym przykładzie zaakceptowano prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6c834-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="6c834-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c834-112">PARAMETERS</span></span>

### <span data-ttu-id="6c834-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c834-113">-DefaultProfile</span></span>
<span data-ttu-id="6c834-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c834-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c834-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="6c834-115">-Description</span></span>
<span data-ttu-id="6c834-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="6c834-116">The reason of action.</span></span>

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

### <span data-ttu-id="6c834-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c834-117">-Name</span></span>
<span data-ttu-id="6c834-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6c834-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c834-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c834-119">-ResourceGroupName</span></span>
<span data-ttu-id="6c834-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c834-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c834-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c834-121">-ResourceId</span></span>
<span data-ttu-id="6c834-122">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="6c834-122">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c834-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6c834-123">-ServiceName</span></span>
<span data-ttu-id="6c834-124">Nazwa usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="6c834-124">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c834-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c834-125">CommonParameters</span></span>
<span data-ttu-id="6c834-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c834-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c834-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c834-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c834-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c834-128">INPUTS</span></span>

### <span data-ttu-id="6c834-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6c834-129">System.String</span></span>

## <span data-ttu-id="6c834-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c834-130">OUTPUTS</span></span>

### <span data-ttu-id="6c834-131">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6c834-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="6c834-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c834-132">NOTES</span></span>

## <span data-ttu-id="6c834-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c834-133">RELATED LINKS</span></span>

[<span data-ttu-id="6c834-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6c834-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6c834-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6c834-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6c834-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6c834-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)