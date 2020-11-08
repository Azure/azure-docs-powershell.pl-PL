---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232848"
---
# <span data-ttu-id="18c2b-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18c2b-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="18c2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="18c2b-103">odmowa połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="18c2b-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="18c2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18c2b-104">SYNTAX</span></span>

### <span data-ttu-id="18c2b-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="18c2b-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18c2b-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="18c2b-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18c2b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="18c2b-107">DESCRIPTION</span></span>
<span data-ttu-id="18c2b-108">Polecenie cmdlet **Deny-AzPrivateEndpointConnection** odrzuca połączenie z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="18c2b-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="18c2b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18c2b-109">EXAMPLES</span></span>

### <span data-ttu-id="18c2b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18c2b-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="18c2b-111">W tym przykładzie odkryto połączenie z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="18c2b-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="18c2b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18c2b-112">PARAMETERS</span></span>

### <span data-ttu-id="18c2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c2b-113">-DefaultProfile</span></span>
<span data-ttu-id="18c2b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18c2b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18c2b-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="18c2b-115">-Description</span></span>
<span data-ttu-id="18c2b-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="18c2b-116">The reason of action.</span></span>

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

### <span data-ttu-id="18c2b-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18c2b-117">-Name</span></span>
<span data-ttu-id="18c2b-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="18c2b-118">The resource name.</span></span>

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

### <span data-ttu-id="18c2b-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="18c2b-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="18c2b-120">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="18c2b-120">The private link resource type.</span></span>

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

### <span data-ttu-id="18c2b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c2b-121">-ResourceGroupName</span></span>
<span data-ttu-id="18c2b-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18c2b-122">The resource group name.</span></span>

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

### <span data-ttu-id="18c2b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18c2b-123">-ResourceId</span></span>
<span data-ttu-id="18c2b-124">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="18c2b-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="18c2b-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="18c2b-125">-ServiceName</span></span>
<span data-ttu-id="18c2b-126">Nazwa usługi, do której należy połączenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="18c2b-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="18c2b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c2b-127">CommonParameters</span></span>
<span data-ttu-id="18c2b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c2b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c2b-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18c2b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c2b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18c2b-130">INPUTS</span></span>

### <span data-ttu-id="18c2b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="18c2b-131">System.String</span></span>

## <span data-ttu-id="18c2b-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18c2b-132">OUTPUTS</span></span>

### <span data-ttu-id="18c2b-133">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18c2b-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="18c2b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18c2b-134">NOTES</span></span>

## <span data-ttu-id="18c2b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18c2b-135">RELATED LINKS</span></span>

[<span data-ttu-id="18c2b-136">Zatwierdzanie — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18c2b-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="18c2b-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18c2b-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="18c2b-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18c2b-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="18c2b-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18c2b-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)