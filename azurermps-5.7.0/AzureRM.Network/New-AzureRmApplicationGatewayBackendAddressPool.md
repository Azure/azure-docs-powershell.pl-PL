---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 7b92f090a4866dabeb064e828dbf3386e26fcb53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545563"
---
# <span data-ttu-id="9fd6e-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fd6e-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="9fd6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fd6e-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd6e-103">Tworzy pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fd6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fd6e-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fd6e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9fd6e-105">DESCRIPTION</span></span>
<span data-ttu-id="9fd6e-106">Polecenie cmdlet **New-AzureRmApplicationGatewayBackendAddressPool** tworzy pulę adresów zaplecza dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="9fd6e-107">Adres zaplecza można określić jako adres IP, w pełni kwalifikowaną nazwę domeny (FQDN) lub Identyfikator konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="9fd6e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fd6e-108">EXAMPLES</span></span>

### <span data-ttu-id="9fd6e-109">Przykład 1. Tworzenie puli adresów zaplecza przy użyciu nazwy FQDN serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="9fd6e-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="9fd6e-110">To polecenie tworzy pulę adresów zaplecza o nazwie Pool01 przy użyciu nazw FQDN serwerów zaplecza i zapisuje ją w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="9fd6e-111">Przykład 2: Tworzenie puli adresów zaplecza przy użyciu adresu IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="9fd6e-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="9fd6e-112">To polecenie tworzy pulę adresów zaplecza o nazwie Pool02 przy użyciu adresów IP serwerów zaplecza i zapisuje ją w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="9fd6e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fd6e-113">PARAMETERS</span></span>

### <span data-ttu-id="9fd6e-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="9fd6e-114">-BackendFqdns</span></span>
<span data-ttu-id="9fd6e-115">Określa listę wewnętrznych nazw FQDN, które to polecenie cmdlet kojarzy z pulą serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd6e-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="9fd6e-116">-BackendIPAddresses</span></span>
<span data-ttu-id="9fd6e-117">Określa listę wewnętrznych adresów IP, które jest skojarzone z tym poleceniem z pulą serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd6e-118">-DefaultProfile</span></span>
<span data-ttu-id="9fd6e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fd6e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fd6e-120">-Name</span></span>
<span data-ttu-id="9fd6e-121">Określa nazwę puli serwerów zaplecza, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd6e-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9fd6e-122">-Confirm</span></span>
<span data-ttu-id="9fd6e-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fd6e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fd6e-124">-WhatIf</span></span>
<span data-ttu-id="9fd6e-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fd6e-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fd6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd6e-127">CommonParameters</span></span>
<span data-ttu-id="9fd6e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd6e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fd6e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd6e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fd6e-130">INPUTS</span></span>

### <span data-ttu-id="9fd6e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9fd6e-131">System.String</span></span>

## <span data-ttu-id="9fd6e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fd6e-132">OUTPUTS</span></span>

### <span data-ttu-id="9fd6e-133">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fd6e-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="9fd6e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fd6e-134">NOTES</span></span>

## <span data-ttu-id="9fd6e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fd6e-135">RELATED LINKS</span></span>

[<span data-ttu-id="9fd6e-136">Dodaj-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fd6e-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9fd6e-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fd6e-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9fd6e-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fd6e-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9fd6e-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fd6e-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


