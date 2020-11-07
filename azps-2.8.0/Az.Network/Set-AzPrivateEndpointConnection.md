---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872184"
---
# <span data-ttu-id="02c01-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="02c01-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="02c01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02c01-102">SYNOPSIS</span></span>
<span data-ttu-id="02c01-103">Aktualizuje stan połączenia prywatnego punktu końcowego w usłudze linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="02c01-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="02c01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02c01-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02c01-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02c01-105">DESCRIPTION</span></span>
<span data-ttu-id="02c01-106">Polecenie cmdlet **Set-AzPrivateEndpointConnection** aktualizuje stan połączenia prywatnego punktu końcowego w usłudze linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="02c01-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="02c01-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02c01-107">EXAMPLES</span></span>

### <span data-ttu-id="02c01-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02c01-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="02c01-109">W tym przykładzie Zaktualizowano stan połączenia prywatnego punktu końcowego na zatwierdzony.</span><span class="sxs-lookup"><span data-stu-id="02c01-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="02c01-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02c01-110">PARAMETERS</span></span>

### <span data-ttu-id="02c01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c01-111">-DefaultProfile</span></span>
<span data-ttu-id="02c01-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02c01-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c01-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="02c01-113">-Description</span></span>
<span data-ttu-id="02c01-114">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="02c01-114">The reason of action.</span></span>

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

### <span data-ttu-id="02c01-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02c01-115">-Name</span></span>
<span data-ttu-id="02c01-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="02c01-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c01-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="02c01-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="02c01-118">Zatwierdzono lub odrzucił zasób.</span><span class="sxs-lookup"><span data-stu-id="02c01-118">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c01-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c01-119">-ResourceGroupName</span></span>
<span data-ttu-id="02c01-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02c01-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c01-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="02c01-121">-ServiceName</span></span>
<span data-ttu-id="02c01-122">Nazwa usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="02c01-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c01-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c01-123">CommonParameters</span></span>
<span data-ttu-id="02c01-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c01-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c01-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02c01-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c01-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02c01-126">INPUTS</span></span>

### <span data-ttu-id="02c01-127">System. String</span><span class="sxs-lookup"><span data-stu-id="02c01-127">System.String</span></span>

## <span data-ttu-id="02c01-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02c01-128">OUTPUTS</span></span>

### <span data-ttu-id="02c01-129">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="02c01-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="02c01-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02c01-130">NOTES</span></span>

## <span data-ttu-id="02c01-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02c01-131">RELATED LINKS</span></span>
