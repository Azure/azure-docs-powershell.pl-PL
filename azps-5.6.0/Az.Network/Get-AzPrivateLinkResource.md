---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 5c341677f5bc741f5848508f80b1a29e29c90b17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954202"
---
# <span data-ttu-id="ae4bd-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ae4bd-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="ae4bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4bd-103">Pobiera prywatny zasób linków.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-103">Gets a private link resource.</span></span>

## <span data-ttu-id="ae4bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae4bd-104">SYNTAX</span></span>

### <span data-ttu-id="ae4bd-105">ByPrivateLinkResourceId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ae4bd-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae4bd-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="ae4bd-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="ae4bd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae4bd-107">DESCRIPTION</span></span>
<span data-ttu-id="ae4bd-108">Polecenie **cmdlet Get-AzPrivateLinkResource** pobiera wszystkie zasoby linków należy do PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="ae4bd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae4bd-109">EXAMPLES</span></span>

### <span data-ttu-id="ae4bd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae4bd-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="ae4bd-111">W tym przykładzie jest lista wszystkich zasobów prywatnych łączy do programu SQL Server o nazwie mySql.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="ae4bd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae4bd-112">PARAMETERS</span></span>

### <span data-ttu-id="ae4bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4bd-113">-DefaultProfile</span></span>
<span data-ttu-id="ae4bd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae4bd-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="ae4bd-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="ae4bd-116">Identyfikator menedżera zasobów platformy Azure dla prywatnego zasobu linków.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-116">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4bd-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="ae4bd-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="ae4bd-118">Typ zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae4bd-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-120">The resource group name.</span></span>

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

### <span data-ttu-id="ae4bd-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ae4bd-121">-ServiceName</span></span>
<span data-ttu-id="ae4bd-122">Nazwa usługi prywatnego linku.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-122">The private link service name.</span></span>

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

### <span data-ttu-id="ae4bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4bd-123">CommonParameters</span></span>
<span data-ttu-id="ae4bd-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4bd-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae4bd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4bd-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae4bd-126">INPUTS</span></span>

### <span data-ttu-id="ae4bd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ae4bd-127">System.String</span></span>

## <span data-ttu-id="ae4bd-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae4bd-128">OUTPUTS</span></span>

### <span data-ttu-id="ae4bd-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae4bd-129">System.Boolean</span></span>

## <span data-ttu-id="ae4bd-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae4bd-130">NOTES</span></span>

## <span data-ttu-id="ae4bd-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae4bd-131">RELATED LINKS</span></span>
