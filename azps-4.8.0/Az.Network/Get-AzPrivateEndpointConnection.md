---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220018"
---
# <span data-ttu-id="e55de-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e55de-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="e55de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e55de-102">SYNOPSIS</span></span>
<span data-ttu-id="e55de-103">Pobiera prywatny zasób połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e55de-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="e55de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e55de-104">SYNTAX</span></span>

### <span data-ttu-id="e55de-105">ByPrivateLinkResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e55de-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e55de-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e55de-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e55de-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="e55de-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e55de-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e55de-108">DESCRIPTION</span></span>
<span data-ttu-id="e55de-109">Polecenie cmdlet **Get-AzPrivateEndpointConnection** pobiera prywatny zasób połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e55de-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="e55de-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e55de-110">EXAMPLES</span></span>

### <span data-ttu-id="e55de-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e55de-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="e55de-112">W tym przykładzie jest zwracana lista wszystkich połączeń prywatnych punktów końcowych z programem SQL Server o nazwie MySQL.</span><span class="sxs-lookup"><span data-stu-id="e55de-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="e55de-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e55de-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="e55de-114">W tym przykładzie uzyskujesz połączenie z prywatnym punktem końcowym o nazwie MyPrivateEndpointConnection1 należy do prywatnej usługi link o nazwie MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e55de-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="e55de-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e55de-115">PARAMETERS</span></span>

### <span data-ttu-id="e55de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e55de-116">-DefaultProfile</span></span>
<span data-ttu-id="e55de-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e55de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e55de-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e55de-118">-Name</span></span>
<span data-ttu-id="e55de-119">Nazwa połączenia prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e55de-119">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e55de-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="e55de-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="e55de-121">Identyfikator Menedżera zasobów platformy Azure zasobu linku prywatnego, do którego należy połączenie prywatne punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e55de-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="e55de-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="e55de-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="e55de-123">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="e55de-123">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e55de-124">-ResourceGroupName</span></span>
<span data-ttu-id="e55de-125">Nazwa grupy zasobów połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="e55de-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e55de-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e55de-126">-ResourceId</span></span>
<span data-ttu-id="e55de-127">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="e55de-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e55de-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e55de-128">-ServiceName</span></span>
<span data-ttu-id="e55de-129">Nazwa usługi, do której należy połączenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e55de-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="e55de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55de-130">CommonParameters</span></span>
<span data-ttu-id="e55de-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e55de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55de-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e55de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55de-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e55de-133">INPUTS</span></span>

### <span data-ttu-id="e55de-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e55de-134">System.String</span></span>

## <span data-ttu-id="e55de-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e55de-135">OUTPUTS</span></span>

### <span data-ttu-id="e55de-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e55de-136">System.Boolean</span></span>

## <span data-ttu-id="e55de-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e55de-137">NOTES</span></span>

## <span data-ttu-id="e55de-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e55de-138">RELATED LINKS</span></span>

[<span data-ttu-id="e55de-139">Zatwierdzanie — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e55de-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e55de-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e55de-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e55de-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e55de-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e55de-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e55de-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
