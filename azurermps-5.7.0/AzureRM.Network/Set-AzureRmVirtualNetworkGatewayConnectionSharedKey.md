---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2f6af6dbbe8a7241cb25e1715859a68bec24598c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542495"
---
# <span data-ttu-id="a337d-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a337d-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="a337d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a337d-102">SYNOPSIS</span></span>
<span data-ttu-id="a337d-103">Konfiguruje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a337d-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a337d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a337d-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a337d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a337d-105">DESCRIPTION</span></span>
<span data-ttu-id="a337d-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** konfiguruje klucz współużytkowany połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a337d-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="a337d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a337d-107">EXAMPLES</span></span>

## <span data-ttu-id="a337d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a337d-108">PARAMETERS</span></span>

### <span data-ttu-id="a337d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a337d-109">-DefaultProfile</span></span>
<span data-ttu-id="a337d-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a337d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a337d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a337d-111">-Force</span></span>
<span data-ttu-id="a337d-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a337d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a337d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a337d-113">-Name</span></span>
<span data-ttu-id="a337d-114">Określa nazwę klucza udostępnionego bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a337d-114">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="a337d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a337d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a337d-116">Określa nazwę grupy zasobów, do której należy Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a337d-116">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="a337d-117">-Value</span><span class="sxs-lookup"><span data-stu-id="a337d-117">-Value</span></span>
<span data-ttu-id="a337d-118">Określa wartość klucza udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="a337d-118">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="a337d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a337d-119">-Confirm</span></span>
<span data-ttu-id="a337d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a337d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a337d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a337d-121">-WhatIf</span></span>
<span data-ttu-id="a337d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a337d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a337d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a337d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a337d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a337d-124">CommonParameters</span></span>
<span data-ttu-id="a337d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a337d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a337d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a337d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a337d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a337d-127">INPUTS</span></span>

### <span data-ttu-id="a337d-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a337d-128">None</span></span>
<span data-ttu-id="a337d-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a337d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a337d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a337d-130">OUTPUTS</span></span>

### <span data-ttu-id="a337d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a337d-131">System.String</span></span>

## <span data-ttu-id="a337d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a337d-132">NOTES</span></span>

## <span data-ttu-id="a337d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a337d-133">RELATED LINKS</span></span>

[<span data-ttu-id="a337d-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a337d-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="a337d-135">Resetowanie — AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a337d-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


