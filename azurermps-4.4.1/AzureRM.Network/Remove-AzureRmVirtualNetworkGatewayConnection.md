---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d2068273c6f46c058ad7586083f6bfa0db037cab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543251"
---
# <span data-ttu-id="9662e-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9662e-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="9662e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9662e-102">SYNOPSIS</span></span>
<span data-ttu-id="9662e-103">Usuwa połączenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9662e-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9662e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9662e-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9662e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9662e-105">DESCRIPTION</span></span>
<span data-ttu-id="9662e-106">Połączenie bramy sieci wirtualnej to obiekt reprezentujący tunel IPsec (lokacja-lokacja lub Sieć wirtualna-wirtualna) połączony z wirtualną bramą sieciową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9662e-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="9662e-107">Polecenie cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** usuwa obiekt połączenia na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9662e-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9662e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9662e-108">EXAMPLES</span></span>

### <span data-ttu-id="9662e-109">1: Usuwanie połączenia bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9662e-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="9662e-110">Usuwa obiekt połączenia bramy sieci wirtualnej o nazwie "mój tunel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="9662e-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="9662e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9662e-111">PARAMETERS</span></span>

### <span data-ttu-id="9662e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9662e-112">-Force</span></span>
<span data-ttu-id="9662e-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9662e-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9662e-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9662e-114">-Name</span></span>
<span data-ttu-id="9662e-115">Określa nazwę połączenia bramy sieci wirtualnej, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9662e-115">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9662e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9662e-116">-PassThru</span></span>
<span data-ttu-id="9662e-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9662e-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9662e-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9662e-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9662e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9662e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9662e-120">Określa nazwę grupy zasobów zawierającej połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9662e-120">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="9662e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9662e-121">-Confirm</span></span>
<span data-ttu-id="9662e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9662e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9662e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9662e-123">-WhatIf</span></span>
<span data-ttu-id="9662e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9662e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9662e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9662e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9662e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9662e-126">-DefaultProfile</span></span>
<span data-ttu-id="9662e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9662e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9662e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9662e-128">CommonParameters</span></span>
<span data-ttu-id="9662e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9662e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9662e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9662e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9662e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9662e-131">INPUTS</span></span>

## <span data-ttu-id="9662e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9662e-132">OUTPUTS</span></span>

## <span data-ttu-id="9662e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9662e-133">NOTES</span></span>

## <span data-ttu-id="9662e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9662e-134">RELATED LINKS</span></span>

[<span data-ttu-id="9662e-135">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9662e-135">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9662e-136">Nowe — AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9662e-136">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9662e-137">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9662e-137">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


