---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3a598001421bf237f93a63fb4f45d069bf9404ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006010"
---
# <span data-ttu-id="7d167-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7d167-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7d167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d167-102">SYNOPSIS</span></span>
<span data-ttu-id="7d167-103">Usuwa połączenie wirtualnej bramy sieciowej</span><span class="sxs-lookup"><span data-stu-id="7d167-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="7d167-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d167-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d167-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d167-105">DESCRIPTION</span></span>
<span data-ttu-id="7d167-106">Połączenie wirtualnej bramy sieciowej to obiekt reprezentujący podprogowy IPsec (Site-to-Site lub Vnet-to-Vnet) połączony z wirtualną bramą sieciową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7d167-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7d167-107">Polecenie **cmdlet Remove-AzVirtualNetworkGatewayConnection** usuwa obiekt połączenia na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d167-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="7d167-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d167-108">EXAMPLES</span></span>

### <span data-ttu-id="7d167-109">Przykład 1. Usuwanie połączenia bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7d167-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="7d167-110">Usuwa obiekt połączenia wirtualnej bramy sieciowej o nazwie "myTunnel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="7d167-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="7d167-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d167-111">PARAMETERS</span></span>

### <span data-ttu-id="7d167-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d167-112">-DefaultProfile</span></span>
<span data-ttu-id="7d167-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d167-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d167-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7d167-114">-Force</span></span>
<span data-ttu-id="7d167-115">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7d167-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d167-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7d167-116">-Name</span></span>
<span data-ttu-id="7d167-117">Określa nazwę połączenia bramy sieci wirtualnej, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d167-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d167-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d167-118">-PassThru</span></span>
<span data-ttu-id="7d167-119">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7d167-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7d167-120">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7d167-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d167-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d167-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d167-122">Określa nazwę grupy zasobów zawierającej połączenie wirtualnej bramy sieciowej.</span><span class="sxs-lookup"><span data-stu-id="7d167-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="7d167-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d167-123">-Confirm</span></span>
<span data-ttu-id="7d167-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7d167-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d167-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d167-125">-WhatIf</span></span>
<span data-ttu-id="7d167-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d167-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d167-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7d167-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d167-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d167-128">CommonParameters</span></span>
<span data-ttu-id="7d167-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d167-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d167-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d167-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d167-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d167-131">INPUTS</span></span>

### <span data-ttu-id="7d167-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7d167-132">System.String</span></span>

## <span data-ttu-id="7d167-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d167-133">OUTPUTS</span></span>

### <span data-ttu-id="7d167-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d167-134">System.Boolean</span></span>

## <span data-ttu-id="7d167-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d167-135">NOTES</span></span>

## <span data-ttu-id="7d167-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d167-136">RELATED LINKS</span></span>

[<span data-ttu-id="7d167-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7d167-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7d167-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7d167-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7d167-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7d167-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
