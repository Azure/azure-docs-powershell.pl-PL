---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: abaaaf7d9f430bd1b7850f3141b651ac02821257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527846"
---
# <span data-ttu-id="99d08-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="99d08-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="99d08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99d08-102">SYNOPSIS</span></span>
<span data-ttu-id="99d08-103">Ta unifiedgroup pobiera zasób połączenia, markę urządzenia sieci VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracyjny, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="99d08-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="99d08-104">Skrypt będzie śledzić składnię wybranego urządzenia i wprowadzić wymagane parametry, takie jak publiczne adresy IP bramy platformy Azure, prefiksy adresów sieci wirtualnej, klucz wstępny tunelu VPN itd., aby klienci mogli po prostu kopiować do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="99d08-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99d08-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99d08-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d08-106">Opis</span><span class="sxs-lookup"><span data-stu-id="99d08-106">DESCRIPTION</span></span>
<span data-ttu-id="99d08-107">Ta unifiedgroup pobiera zasób połączenia, markę urządzenia sieci VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracyjny, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="99d08-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="99d08-108">Skrypt będzie śledzić składnię wybranego urządzenia i wprowadzić wymagane parametry, takie jak publiczne adresy IP bramy platformy Azure, prefiksy adresów sieci wirtualnej, klucz wstępny tunelu VPN itd., aby klienci mogli po prostu kopiować do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="99d08-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="99d08-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99d08-109">EXAMPLES</span></span>

### <span data-ttu-id="99d08-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99d08-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="99d08-111">W powyższym przykładzie użyto Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice, aby uzyskać obsługiwane marki, modele i wersje oprogramowania wewnętrznego urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="99d08-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="99d08-112">Następnie używa jednej ze zwróconych informacji o modelach w celu wygenerowania skryptu konfiguracji urządzenia sieci VPN dla VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="99d08-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="99d08-113">Urządzenie używane w tym przykładzie ma DeviceFamily "IOS-test", DeviceVendor "Cisco-test" i FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="99d08-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="99d08-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99d08-114">PARAMETERS</span></span>

### <span data-ttu-id="99d08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d08-115">-DefaultProfile</span></span>
<span data-ttu-id="99d08-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99d08-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99d08-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="99d08-117">-DeviceFamily</span></span>
<span data-ttu-id="99d08-118">Nazwa modelu/rodziny urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="99d08-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="99d08-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="99d08-119">-DeviceVendor</span></span>
<span data-ttu-id="99d08-120">Nazwa dostawcy urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="99d08-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="99d08-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="99d08-121">-FirmwareVersion</span></span>
<span data-ttu-id="99d08-122">Wersja oprogramowania układowego urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="99d08-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="99d08-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99d08-123">-Name</span></span>
<span data-ttu-id="99d08-124">Nazwa zasobu połączenia, dla którego ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="99d08-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="99d08-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d08-125">-ResourceGroupName</span></span>
<span data-ttu-id="99d08-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99d08-126">The resource group name.</span></span>

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

### <span data-ttu-id="99d08-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99d08-127">-Confirm</span></span>
<span data-ttu-id="99d08-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d08-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d08-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d08-129">-WhatIf</span></span>
<span data-ttu-id="99d08-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d08-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d08-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99d08-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d08-132">CommonParameters</span></span>
<span data-ttu-id="99d08-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d08-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d08-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d08-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99d08-135">INPUTS</span></span>

### <span data-ttu-id="99d08-136">System. String</span><span class="sxs-lookup"><span data-stu-id="99d08-136">System.String</span></span>

## <span data-ttu-id="99d08-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99d08-137">OUTPUTS</span></span>

### <span data-ttu-id="99d08-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99d08-138">System.String</span></span>

## <span data-ttu-id="99d08-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99d08-139">NOTES</span></span>

## <span data-ttu-id="99d08-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99d08-140">RELATED LINKS</span></span>
