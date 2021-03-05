---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: c331cbb9731024598fe4d2542e734e406ac144ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993539"
---
# <span data-ttu-id="cb521-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cb521-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="cb521-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb521-102">SYNOPSIS</span></span>
<span data-ttu-id="cb521-103">Usuwa istniejącą bramę P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cb521-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="cb521-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb521-104">SYNTAX</span></span>

### <span data-ttu-id="cb521-105">ByP2SVpnGatewayName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cb521-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb521-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cb521-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb521-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cb521-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb521-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb521-108">DESCRIPTION</span></span>
<span data-ttu-id="cb521-109">Polecenie **cmdlet Remove-AzP2sVpnGateway** umożliwia usunięcie istniejącej aplikacji P2SVpnGateway w obszarze VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="cb521-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="cb521-110">Wszystkie point to site clients connectivity will fail after P2SVpnGateway is removed.</span><span class="sxs-lookup"><span data-stu-id="cb521-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="cb521-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb521-111">EXAMPLES</span></span>

### <span data-ttu-id="cb521-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb521-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="cb521-113">Polecenie **cmdlet Remove-AzP2sVpnGateway** umożliwia usunięcie istniejącej aplikacji P2SVpnGateway w obszarze VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="cb521-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="cb521-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb521-114">PARAMETERS</span></span>

### <span data-ttu-id="cb521-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb521-115">-DefaultProfile</span></span>
<span data-ttu-id="cb521-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb521-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cb521-117">-Force</span></span>
<span data-ttu-id="cb521-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb521-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb521-119">-InputObject</span></span>
<span data-ttu-id="cb521-120">Obiekt p2sVpnGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cb521-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cb521-121">-Name</span></span>
<span data-ttu-id="cb521-122">Nazwa aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cb521-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb521-123">-PassThru</span></span>
<span data-ttu-id="cb521-124">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="cb521-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb521-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb521-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb521-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb521-127">-ResourceId</span></span>
<span data-ttu-id="cb521-128">Identyfikator zasobu Azure dla aplikacji p2sVpnGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cb521-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb521-129">-Confirm</span></span>
<span data-ttu-id="cb521-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb521-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb521-131">-WhatIf</span></span>
<span data-ttu-id="cb521-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb521-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb521-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cb521-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb521-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb521-134">CommonParameters</span></span>
<span data-ttu-id="cb521-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb521-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb521-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb521-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb521-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb521-137">INPUTS</span></span>

### <span data-ttu-id="cb521-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cb521-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="cb521-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cb521-139">System.String</span></span>

## <span data-ttu-id="cb521-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb521-140">OUTPUTS</span></span>

### <span data-ttu-id="cb521-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb521-141">System.Boolean</span></span>

## <span data-ttu-id="cb521-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb521-142">NOTES</span></span>

## <span data-ttu-id="cb521-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb521-143">RELATED LINKS</span></span>
