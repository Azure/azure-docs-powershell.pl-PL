---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202555"
---
# <span data-ttu-id="97ba1-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="97ba1-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="97ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="97ba1-103">Usuwa istniejącą bramę P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="97ba1-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="97ba1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97ba1-104">SYNTAX</span></span>

### <span data-ttu-id="97ba1-105">ByP2SVpnGatewayName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="97ba1-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97ba1-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="97ba1-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97ba1-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="97ba1-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97ba1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="97ba1-108">DESCRIPTION</span></span>
<span data-ttu-id="97ba1-109">Polecenie **cmdlet Remove-AzP2sVpnGateway** umożliwia usunięcie istniejącej aplikacji P2SVpnGateway w obszarze VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="97ba1-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="97ba1-110">Po usunięciu aplikacji P2SVpnGateway cały punkt łączności klientów witryny nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="97ba1-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="97ba1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97ba1-111">EXAMPLES</span></span>

### <span data-ttu-id="97ba1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97ba1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="97ba1-113">Polecenie **cmdlet Remove-AzP2sVpnGateway** umożliwia usunięcie istniejącej aplikacji P2SVpnGateway w obszarze VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="97ba1-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="97ba1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97ba1-114">PARAMETERS</span></span>

### <span data-ttu-id="97ba1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ba1-115">-DefaultProfile</span></span>
<span data-ttu-id="97ba1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97ba1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97ba1-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="97ba1-117">-Force</span></span>
<span data-ttu-id="97ba1-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97ba1-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="97ba1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97ba1-119">-InputObject</span></span>
<span data-ttu-id="97ba1-120">Obiekt p2sVpnGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="97ba1-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="97ba1-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="97ba1-121">-Name</span></span>
<span data-ttu-id="97ba1-122">Nazwa aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="97ba1-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="97ba1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97ba1-123">-PassThru</span></span>
<span data-ttu-id="97ba1-124">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="97ba1-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="97ba1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ba1-125">-ResourceGroupName</span></span>
<span data-ttu-id="97ba1-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97ba1-126">The resource group name.</span></span>

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

### <span data-ttu-id="97ba1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97ba1-127">-ResourceId</span></span>
<span data-ttu-id="97ba1-128">Identyfikator zasobu Azure dla aplikacji p2sVpnGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="97ba1-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="97ba1-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97ba1-129">-Confirm</span></span>
<span data-ttu-id="97ba1-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97ba1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97ba1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97ba1-131">-WhatIf</span></span>
<span data-ttu-id="97ba1-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97ba1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97ba1-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="97ba1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97ba1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ba1-134">CommonParameters</span></span>
<span data-ttu-id="97ba1-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ba1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ba1-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ba1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ba1-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97ba1-137">INPUTS</span></span>

### <span data-ttu-id="97ba1-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="97ba1-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="97ba1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="97ba1-139">System.String</span></span>

## <span data-ttu-id="97ba1-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97ba1-140">OUTPUTS</span></span>

### <span data-ttu-id="97ba1-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="97ba1-141">System.Boolean</span></span>

## <span data-ttu-id="97ba1-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97ba1-142">NOTES</span></span>

## <span data-ttu-id="97ba1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97ba1-143">RELATED LINKS</span></span>
