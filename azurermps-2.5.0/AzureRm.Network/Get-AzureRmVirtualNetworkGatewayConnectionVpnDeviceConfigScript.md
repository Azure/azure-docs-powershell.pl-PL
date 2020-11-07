---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
ms.openlocfilehash: 0565956d7f40a633bc1aa2c2049ef9a7d764d77e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898900"
---
# <span data-ttu-id="0db34-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="0db34-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="0db34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0db34-102">SYNOPSIS</span></span>
<span data-ttu-id="0db34-103">Ta unifiedgroup pobiera zasób połączenia, markę urządzenia sieci VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracyjny, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="0db34-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="0db34-104">Skrypt będzie śledzić składnię wybranego urządzenia i wprowadzić wymagane parametry, takie jak publiczne adresy IP bramy platformy Azure, prefiksy adresów sieci wirtualnej, klucz wstępny tunelu VPN itd., aby klienci mogli po prostu kopiować do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="0db34-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0db34-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0db34-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db34-106">Opis</span><span class="sxs-lookup"><span data-stu-id="0db34-106">DESCRIPTION</span></span>
<span data-ttu-id="0db34-107">Ta unifiedgroup pobiera zasób połączenia, markę urządzenia sieci VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracyjny, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="0db34-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="0db34-108">Skrypt będzie śledzić składnię wybranego urządzenia i wprowadzić wymagane parametry, takie jak publiczne adresy IP bramy platformy Azure, prefiksy adresów sieci wirtualnej, klucz wstępny tunelu VPN itd., aby klienci mogli po prostu kopiować do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="0db34-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="0db34-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0db34-109">EXAMPLES</span></span>

### <span data-ttu-id="0db34-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0db34-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="0db34-111">W powyższym przykładzie użyto Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice, aby uzyskać obsługiwane marki, modele i wersje oprogramowania wewnętrznego urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="0db34-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="0db34-112">Następnie używa jednej ze zwróconych informacji o modelach w celu wygenerowania skryptu konfiguracji urządzenia sieci VPN dla VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="0db34-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="0db34-113">Urządzenie używane w tym przykładzie ma DeviceFamily "IOS-test", DeviceVendor "Cisco-test" i FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="0db34-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="0db34-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0db34-114">PARAMETERS</span></span>

### <span data-ttu-id="0db34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db34-115">-DefaultProfile</span></span>
<span data-ttu-id="0db34-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0db34-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0db34-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="0db34-117">-DeviceFamily</span></span>
<span data-ttu-id="0db34-118">Nazwa modelu/rodziny urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="0db34-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="0db34-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="0db34-119">-DeviceVendor</span></span>
<span data-ttu-id="0db34-120">Nazwa dostawcy urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="0db34-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="0db34-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="0db34-121">-FirmwareVersion</span></span>
<span data-ttu-id="0db34-122">Wersja oprogramowania układowego urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="0db34-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="0db34-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0db34-123">-Name</span></span>
<span data-ttu-id="0db34-124">Nazwa zasobu połączenia, dla którego ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="0db34-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="0db34-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db34-125">-ResourceGroupName</span></span>
<span data-ttu-id="0db34-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0db34-126">The resource group name.</span></span>

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

### <span data-ttu-id="0db34-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0db34-127">-Confirm</span></span>
<span data-ttu-id="0db34-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0db34-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db34-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db34-129">-WhatIf</span></span>
<span data-ttu-id="0db34-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0db34-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db34-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0db34-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db34-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db34-132">CommonParameters</span></span>
<span data-ttu-id="0db34-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db34-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db34-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db34-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db34-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0db34-135">INPUTS</span></span>

### <span data-ttu-id="0db34-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0db34-136">System.String</span></span>

## <span data-ttu-id="0db34-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0db34-137">OUTPUTS</span></span>

### <span data-ttu-id="0db34-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0db34-138">System.String</span></span>

## <span data-ttu-id="0db34-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0db34-139">NOTES</span></span>

## <span data-ttu-id="0db34-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0db34-140">RELATED LINKS</span></span>

