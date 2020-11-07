---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 70d110e9a539661d780c2dbce7fb8166a8f4ba97
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892914"
---
# <span data-ttu-id="47dce-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="47dce-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="47dce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47dce-102">SYNOPSIS</span></span>
<span data-ttu-id="47dce-103">Usuwa połączenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="47dce-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="47dce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47dce-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47dce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47dce-105">DESCRIPTION</span></span>
<span data-ttu-id="47dce-106">Połączenie bramy sieci wirtualnej to obiekt reprezentujący tunel IPsec (lokacja-lokacja lub Sieć wirtualna-wirtualna) połączony z wirtualną bramą sieciową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="47dce-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="47dce-107">Polecenie cmdlet **Remove-AzVirtualNetworkGatewayConnection** usuwa obiekt połączenia na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47dce-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="47dce-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47dce-108">EXAMPLES</span></span>

### <span data-ttu-id="47dce-109">1: Usuwanie połączenia bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="47dce-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="47dce-110">Usuwa obiekt połączenia bramy sieci wirtualnej o nazwie "mój tunel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="47dce-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="47dce-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47dce-111">PARAMETERS</span></span>

### <span data-ttu-id="47dce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dce-112">-DefaultProfile</span></span>
<span data-ttu-id="47dce-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47dce-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dce-114">-Force</span><span class="sxs-lookup"><span data-stu-id="47dce-114">-Force</span></span>
<span data-ttu-id="47dce-115">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="47dce-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="47dce-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47dce-116">-Name</span></span>
<span data-ttu-id="47dce-117">Określa nazwę połączenia bramy sieci wirtualnej, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47dce-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47dce-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47dce-118">-PassThru</span></span>
<span data-ttu-id="47dce-119">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="47dce-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="47dce-120">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="47dce-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="47dce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47dce-121">-ResourceGroupName</span></span>
<span data-ttu-id="47dce-122">Określa nazwę grupy zasobów zawierającej połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="47dce-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47dce-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47dce-123">-Confirm</span></span>
<span data-ttu-id="47dce-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47dce-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dce-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47dce-125">-WhatIf</span></span>
<span data-ttu-id="47dce-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47dce-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47dce-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47dce-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dce-128">CommonParameters</span></span>
<span data-ttu-id="47dce-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47dce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dce-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47dce-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dce-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47dce-131">INPUTS</span></span>

## <span data-ttu-id="47dce-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47dce-132">OUTPUTS</span></span>

## <span data-ttu-id="47dce-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47dce-133">NOTES</span></span>

## <span data-ttu-id="47dce-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47dce-134">RELATED LINKS</span></span>

[<span data-ttu-id="47dce-135">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="47dce-135">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="47dce-136">Nowe — AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="47dce-136">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="47dce-137">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="47dce-137">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)


