---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: c8e0e5a3d503b4fa587f2a0bdb284b059bff4eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993658"
---
# <span data-ttu-id="ff3dc-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ff3dc-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="ff3dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff3dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3dc-103">Usuwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="ff3dc-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="ff3dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff3dc-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff3dc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff3dc-105">DESCRIPTION</span></span>
<span data-ttu-id="ff3dc-106">Lokalna brama sieciowa to obiekt reprezentujący lokalne urządzenie sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="ff3dc-107">Polecenie **cmdlet Remove-AzLocalNetworkGateway** usuwa obiekt reprezentujący wejściową bramę na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ff3dc-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff3dc-108">EXAMPLES</span></span>

### <span data-ttu-id="ff3dc-109">Przykład 1. Usuwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="ff3dc-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="ff3dc-110">Usuwa obiekt lokalnej bramy sieciowej o nazwie "myLocalGW" w grupie zasobów "myRG" Uwaga: Należy najpierw usunąć wszystkie połączenia z bramą sieci lokalnej przy użyciu polecenia cmdlet **Remove-AzVirtualNetworkGatewayConnection.**</span><span class="sxs-lookup"><span data-stu-id="ff3dc-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="ff3dc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff3dc-111">PARAMETERS</span></span>

### <span data-ttu-id="ff3dc-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ff3dc-112">-AsJob</span></span>
<span data-ttu-id="ff3dc-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ff3dc-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3dc-114">-DefaultProfile</span></span>
<span data-ttu-id="ff3dc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff3dc-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ff3dc-116">-Force</span></span>
<span data-ttu-id="ff3dc-117">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3dc-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff3dc-118">-Name</span></span>
<span data-ttu-id="ff3dc-119">Określa nazwę lokalnej bramy sieciowej, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ff3dc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff3dc-120">-PassThru</span></span>
<span data-ttu-id="ff3dc-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ff3dc-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff3dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff3dc-124">Określa nazwę grupy zasobów zawierającej lokalną bramę sieciową.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="ff3dc-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff3dc-125">-Confirm</span></span>
<span data-ttu-id="ff3dc-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3dc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3dc-127">-WhatIf</span></span>
<span data-ttu-id="ff3dc-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff3dc-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3dc-130">CommonParameters</span></span>
<span data-ttu-id="ff3dc-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3dc-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff3dc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3dc-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff3dc-133">INPUTS</span></span>

### <span data-ttu-id="ff3dc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ff3dc-134">System.String</span></span>

## <span data-ttu-id="ff3dc-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff3dc-135">OUTPUTS</span></span>

### <span data-ttu-id="ff3dc-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff3dc-136">System.Boolean</span></span>

## <span data-ttu-id="ff3dc-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff3dc-137">NOTES</span></span>

## <span data-ttu-id="ff3dc-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff3dc-138">RELATED LINKS</span></span>

[<span data-ttu-id="ff3dc-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ff3dc-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="ff3dc-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ff3dc-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="ff3dc-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ff3dc-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
