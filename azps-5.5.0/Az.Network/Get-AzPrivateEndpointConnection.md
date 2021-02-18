---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184730"
---
# <span data-ttu-id="a22b6-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a22b6-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="a22b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a22b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a22b6-103">Pobiera prywatny zasób połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a22b6-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="a22b6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a22b6-104">SYNTAX</span></span>

### <span data-ttu-id="a22b6-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="a22b6-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a22b6-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a22b6-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a22b6-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="a22b6-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a22b6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a22b6-108">DESCRIPTION</span></span>
<span data-ttu-id="a22b6-109">Polecenie **cmdlet Get-AzPrivateEndpointConnection** pobiera prywatny zasób połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a22b6-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="a22b6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a22b6-110">EXAMPLES</span></span>

### <span data-ttu-id="a22b6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a22b6-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="a22b6-112">Ten przykład zwraca listę wszystkich prywatnych połączeń punktu końcowego należy do serwera sql o nazwie Mysql.</span><span class="sxs-lookup"><span data-stu-id="a22b6-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="a22b6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a22b6-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="a22b6-114">W tym przykładzie jest uzyskiwanie prywatnego połączenia punktu końcowego o nazwie MyPrivateEndpointConnection1 należy do prywatnej usługi łączenia o nazwie MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a22b6-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="a22b6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a22b6-115">PARAMETERS</span></span>

### <span data-ttu-id="a22b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a22b6-116">-DefaultProfile</span></span>
<span data-ttu-id="a22b6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a22b6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a22b6-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="a22b6-118">-Description</span></span>
<span data-ttu-id="a22b6-119">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="a22b6-119">The reason of action.</span></span>

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

### <span data-ttu-id="a22b6-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a22b6-120">-Name</span></span>
<span data-ttu-id="a22b6-121">Nazwa prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a22b6-121">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22b6-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a22b6-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a22b6-123">Identyfikator menedżera zasobów platformy Azure dla prywatnego zasobu linku, do którego należy prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a22b6-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="a22b6-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="a22b6-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="a22b6-125">Typ zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="a22b6-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a22b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a22b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="a22b6-127">Nazwa grupy zasobów dla prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a22b6-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a22b6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a22b6-128">-ResourceId</span></span>
<span data-ttu-id="a22b6-129">Identyfikator menedżera zasobów platformy Azure prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a22b6-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a22b6-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a22b6-130">-ServiceName</span></span>
<span data-ttu-id="a22b6-131">Nazwa usługi, do której należy prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="a22b6-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="a22b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22b6-132">CommonParameters</span></span>
<span data-ttu-id="a22b6-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a22b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22b6-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a22b6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22b6-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a22b6-135">INPUTS</span></span>

### <span data-ttu-id="a22b6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a22b6-136">System.String</span></span>

## <span data-ttu-id="a22b6-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a22b6-137">OUTPUTS</span></span>

### <span data-ttu-id="a22b6-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a22b6-138">System.Boolean</span></span>

## <span data-ttu-id="a22b6-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a22b6-139">NOTES</span></span>

## <span data-ttu-id="a22b6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a22b6-140">RELATED LINKS</span></span>

[<span data-ttu-id="a22b6-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a22b6-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a22b6-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a22b6-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a22b6-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a22b6-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a22b6-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a22b6-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
