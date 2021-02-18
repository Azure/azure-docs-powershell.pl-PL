---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184722"
---
# <span data-ttu-id="a6935-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a6935-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="a6935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6935-102">SYNOPSIS</span></span>
<span data-ttu-id="a6935-103">Pobiera prywatny zasób linków.</span><span class="sxs-lookup"><span data-stu-id="a6935-103">Gets a private link resource.</span></span>

## <span data-ttu-id="a6935-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6935-104">SYNTAX</span></span>

### <span data-ttu-id="a6935-105">ByPrivateLinkResourceId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a6935-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6935-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="a6935-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="a6935-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6935-107">DESCRIPTION</span></span>
<span data-ttu-id="a6935-108">Polecenie **cmdlet Get-AzPrivateLinkResource** pobiera wszystkie zasoby linków należy do PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="a6935-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="a6935-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6935-109">EXAMPLES</span></span>

### <span data-ttu-id="a6935-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6935-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="a6935-111">W tym przykładzie jest lista wszystkich zasobów prywatnych łączy do programu SQL Server o nazwie mySql.</span><span class="sxs-lookup"><span data-stu-id="a6935-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="a6935-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6935-112">PARAMETERS</span></span>

### <span data-ttu-id="a6935-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6935-113">-DefaultProfile</span></span>
<span data-ttu-id="a6935-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6935-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6935-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a6935-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a6935-116">Identyfikator menedżera zasobów platformy Azure dla prywatnego zasobu linków.</span><span class="sxs-lookup"><span data-stu-id="a6935-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="a6935-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="a6935-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="a6935-118">Typ zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="a6935-118">The private link resource type.</span></span>

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

### <span data-ttu-id="a6935-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6935-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6935-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6935-120">The resource group name.</span></span>

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

### <span data-ttu-id="a6935-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a6935-121">-ServiceName</span></span>
<span data-ttu-id="a6935-122">Nazwa usługi prywatnego linku.</span><span class="sxs-lookup"><span data-stu-id="a6935-122">The private link service name.</span></span>

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

### <span data-ttu-id="a6935-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6935-123">CommonParameters</span></span>
<span data-ttu-id="a6935-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6935-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6935-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6935-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6935-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6935-126">INPUTS</span></span>

### <span data-ttu-id="a6935-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a6935-127">System.String</span></span>

## <span data-ttu-id="a6935-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6935-128">OUTPUTS</span></span>

### <span data-ttu-id="a6935-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6935-129">System.Boolean</span></span>

## <span data-ttu-id="a6935-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6935-130">NOTES</span></span>

## <span data-ttu-id="a6935-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6935-131">RELATED LINKS</span></span>
