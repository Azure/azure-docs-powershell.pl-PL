---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319152"
---
# <span data-ttu-id="bdff2-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bdff2-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="bdff2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdff2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdff2-103">Usuwa istniejące P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bdff2-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="bdff2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdff2-104">SYNTAX</span></span>

### <span data-ttu-id="bdff2-105">ByP2SVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bdff2-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdff2-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="bdff2-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdff2-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="bdff2-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdff2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bdff2-108">DESCRIPTION</span></span>
<span data-ttu-id="bdff2-109">Polecenie cmdlet **Remove-AzP2sVpnGateway** umożliwia usunięcie istniejącego P2SVpnGateway w obszarze VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="bdff2-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="bdff2-110">Po usunięciu P2SVpnGateway wszyscy klienci witryny nie będą mogli nawiązać połączenia z siecią.</span><span class="sxs-lookup"><span data-stu-id="bdff2-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="bdff2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdff2-111">EXAMPLES</span></span>

### <span data-ttu-id="bdff2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bdff2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="bdff2-113">Polecenie cmdlet **Remove-AzP2sVpnGateway** umożliwia usunięcie istniejącego P2SVpnGateway w obszarze VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="bdff2-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="bdff2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdff2-114">PARAMETERS</span></span>

### <span data-ttu-id="bdff2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdff2-115">-DefaultProfile</span></span>
<span data-ttu-id="bdff2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdff2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdff2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bdff2-117">-Force</span></span>
<span data-ttu-id="bdff2-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bdff2-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bdff2-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bdff2-119">-InputObject</span></span>
<span data-ttu-id="bdff2-120">Obiekt p2sVpnGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="bdff2-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="bdff2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdff2-121">-Name</span></span>
<span data-ttu-id="bdff2-122">Nazwa P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bdff2-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="bdff2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdff2-123">-PassThru</span></span>
<span data-ttu-id="bdff2-124">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="bdff2-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="bdff2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdff2-125">-ResourceGroupName</span></span>
<span data-ttu-id="bdff2-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdff2-126">The resource group name.</span></span>

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

### <span data-ttu-id="bdff2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdff2-127">-ResourceId</span></span>
<span data-ttu-id="bdff2-128">Identyfikator zasobu platformy Azure dla p2sVpnGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="bdff2-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="bdff2-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdff2-129">-Confirm</span></span>
<span data-ttu-id="bdff2-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdff2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdff2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdff2-131">-WhatIf</span></span>
<span data-ttu-id="bdff2-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdff2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdff2-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdff2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdff2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdff2-134">CommonParameters</span></span>
<span data-ttu-id="bdff2-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdff2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdff2-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdff2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdff2-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdff2-137">INPUTS</span></span>

### <span data-ttu-id="bdff2-138">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bdff2-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="bdff2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bdff2-139">System.String</span></span>

## <span data-ttu-id="bdff2-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdff2-140">OUTPUTS</span></span>

### <span data-ttu-id="bdff2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdff2-141">System.Boolean</span></span>

## <span data-ttu-id="bdff2-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdff2-142">NOTES</span></span>

## <span data-ttu-id="bdff2-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdff2-143">RELATED LINKS</span></span>
