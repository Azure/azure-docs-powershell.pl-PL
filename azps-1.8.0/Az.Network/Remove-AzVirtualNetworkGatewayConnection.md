---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3a2cd6b4fd4cefdfda10e3491aef31ed9a138383
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709071"
---
# <span data-ttu-id="54d0b-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54d0b-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="54d0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="54d0b-103">Usuwa połączenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="54d0b-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="54d0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54d0b-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d0b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="54d0b-105">DESCRIPTION</span></span>
<span data-ttu-id="54d0b-106">Połączenie bramy sieci wirtualnej to obiekt reprezentujący tunel IPsec (lokacja-lokacja lub Sieć wirtualna-wirtualna) połączony z wirtualną bramą sieciową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="54d0b-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="54d0b-107">Polecenie cmdlet **Remove-AzVirtualNetworkGatewayConnection** usuwa obiekt połączenia na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54d0b-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="54d0b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54d0b-108">EXAMPLES</span></span>

### <span data-ttu-id="54d0b-109">1: Usuwanie połączenia bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="54d0b-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="54d0b-110">Usuwa obiekt połączenia bramy sieci wirtualnej o nazwie "mój tunel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="54d0b-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="54d0b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54d0b-111">PARAMETERS</span></span>

### <span data-ttu-id="54d0b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d0b-112">-DefaultProfile</span></span>
<span data-ttu-id="54d0b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54d0b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54d0b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="54d0b-114">-Force</span></span>
<span data-ttu-id="54d0b-115">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="54d0b-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54d0b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54d0b-116">-Name</span></span>
<span data-ttu-id="54d0b-117">Określa nazwę połączenia bramy sieci wirtualnej, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d0b-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="54d0b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54d0b-118">-PassThru</span></span>
<span data-ttu-id="54d0b-119">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="54d0b-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="54d0b-120">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="54d0b-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54d0b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d0b-121">-ResourceGroupName</span></span>
<span data-ttu-id="54d0b-122">Określa nazwę grupy zasobów zawierającej połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="54d0b-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="54d0b-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54d0b-123">-Confirm</span></span>
<span data-ttu-id="54d0b-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d0b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d0b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d0b-125">-WhatIf</span></span>
<span data-ttu-id="54d0b-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d0b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54d0b-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="54d0b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d0b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d0b-128">CommonParameters</span></span>
<span data-ttu-id="54d0b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d0b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d0b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d0b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d0b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54d0b-131">INPUTS</span></span>

### <span data-ttu-id="54d0b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="54d0b-132">System.String</span></span>

## <span data-ttu-id="54d0b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54d0b-133">OUTPUTS</span></span>

### <span data-ttu-id="54d0b-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54d0b-134">System.Boolean</span></span>

## <span data-ttu-id="54d0b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54d0b-135">NOTES</span></span>

## <span data-ttu-id="54d0b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54d0b-136">RELATED LINKS</span></span>

[<span data-ttu-id="54d0b-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54d0b-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="54d0b-138">Nowe — AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54d0b-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="54d0b-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54d0b-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)