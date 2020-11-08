---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052274"
---
# <span data-ttu-id="94b7b-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94b7b-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="94b7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="94b7b-103">Pobiera prywatny zasób połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="94b7b-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="94b7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94b7b-104">SYNTAX</span></span>

### <span data-ttu-id="94b7b-105">ByPrivateLinkResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="94b7b-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="94b7b-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7b-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="94b7b-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94b7b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="94b7b-108">DESCRIPTION</span></span>
<span data-ttu-id="94b7b-109">Polecenie cmdlet **Get-AzPrivateEndpointConnection** pobiera prywatny zasób połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="94b7b-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="94b7b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94b7b-110">EXAMPLES</span></span>

### <span data-ttu-id="94b7b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94b7b-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="94b7b-112">W tym przykładzie jest zwracana lista wszystkich połączeń prywatnych punktów końcowych z programem SQL Server o nazwie MySQL.</span><span class="sxs-lookup"><span data-stu-id="94b7b-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="94b7b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="94b7b-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="94b7b-114">W tym przykładzie uzyskujesz połączenie z prywatnym punktem końcowym o nazwie MyPrivateEndpointConnection1 należy do prywatnej usługi link o nazwie MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="94b7b-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="94b7b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94b7b-115">PARAMETERS</span></span>

### <span data-ttu-id="94b7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b7b-116">-DefaultProfile</span></span>
<span data-ttu-id="94b7b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94b7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94b7b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94b7b-118">-Name</span></span>
<span data-ttu-id="94b7b-119">Nazwa połączenia prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="94b7b-119">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="94b7b-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="94b7b-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="94b7b-121">Identyfikator Menedżera zasobów platformy Azure zasobu linku prywatnego, do którego należy połączenie prywatne punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="94b7b-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="94b7b-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="94b7b-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="94b7b-123">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="94b7b-123">The private link resource type.</span></span>

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

### <span data-ttu-id="94b7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="94b7b-125">Nazwa grupy zasobów połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="94b7b-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="94b7b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94b7b-126">-ResourceId</span></span>
<span data-ttu-id="94b7b-127">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="94b7b-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="94b7b-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="94b7b-128">-ServiceName</span></span>
<span data-ttu-id="94b7b-129">Nazwa usługi, do której należy połączenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="94b7b-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="94b7b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b7b-130">CommonParameters</span></span>
<span data-ttu-id="94b7b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b7b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b7b-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94b7b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b7b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94b7b-133">INPUTS</span></span>

### <span data-ttu-id="94b7b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="94b7b-134">System.String</span></span>

## <span data-ttu-id="94b7b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94b7b-135">OUTPUTS</span></span>

### <span data-ttu-id="94b7b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94b7b-136">System.Boolean</span></span>

## <span data-ttu-id="94b7b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94b7b-137">NOTES</span></span>

## <span data-ttu-id="94b7b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94b7b-138">RELATED LINKS</span></span>

[<span data-ttu-id="94b7b-139">Zatwierdzanie — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94b7b-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="94b7b-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94b7b-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="94b7b-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94b7b-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="94b7b-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94b7b-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
