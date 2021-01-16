---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335617"
---
# <span data-ttu-id="27b4a-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="27b4a-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="27b4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="27b4a-103">Ta unifiedgroup pobiera zasób połączenia, markę urządzenia sieci VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracyjny, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="27b4a-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="27b4a-104">Skrypt będzie śledzić składnię wybranego urządzenia i wprowadzić wymagane parametry, takie jak publiczne adresy IP bramy platformy Azure, prefiksy adresów sieci wirtualnej, klucz wstępny tunelu VPN itd., aby klienci mogli po prostu kopiować do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="27b4a-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="27b4a-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27b4a-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b4a-106">Opis</span><span class="sxs-lookup"><span data-stu-id="27b4a-106">DESCRIPTION</span></span>
<span data-ttu-id="27b4a-107">Ta unifiedgroup pobiera zasób połączenia, markę urządzenia sieci VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracyjny, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="27b4a-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="27b4a-108">Skrypt będzie śledzić składnię wybranego urządzenia i wprowadzić wymagane parametry, takie jak publiczne adresy IP bramy platformy Azure, prefiksy adresów sieci wirtualnej, klucz wstępny tunelu VPN itd., aby klienci mogli po prostu kopiować do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="27b4a-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="27b4a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27b4a-109">EXAMPLES</span></span>

### <span data-ttu-id="27b4a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27b4a-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="27b4a-111">W powyższym przykładzie użyto Get-AzVirtualNetworkGatewaySupportedVpnDevice, aby uzyskać obsługiwane marki, modele i wersje oprogramowania wewnętrznego urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="27b4a-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="27b4a-112">Następnie używa jednej ze zwróconych informacji o modelach w celu wygenerowania skryptu konfiguracji urządzenia sieci VPN dla VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="27b4a-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="27b4a-113">Urządzenie używane w tym przykładzie ma DeviceFamily "IOS-test", DeviceVendor "Cisco-test" i FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="27b4a-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="27b4a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27b4a-114">PARAMETERS</span></span>

### <span data-ttu-id="27b4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b4a-115">-DefaultProfile</span></span>
<span data-ttu-id="27b4a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27b4a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27b4a-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="27b4a-117">-DeviceFamily</span></span>
<span data-ttu-id="27b4a-118">Nazwa modelu/rodziny urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="27b4a-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="27b4a-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="27b4a-119">-DeviceVendor</span></span>
<span data-ttu-id="27b4a-120">Nazwa dostawcy urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="27b4a-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="27b4a-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="27b4a-121">-FirmwareVersion</span></span>
<span data-ttu-id="27b4a-122">Wersja oprogramowania układowego urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="27b4a-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="27b4a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="27b4a-123">-Name</span></span>
<span data-ttu-id="27b4a-124">Nazwa zasobu połączenia, dla którego ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="27b4a-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="27b4a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b4a-125">-ResourceGroupName</span></span>
<span data-ttu-id="27b4a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="27b4a-126">The resource group name.</span></span>

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

### <span data-ttu-id="27b4a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27b4a-127">-Confirm</span></span>
<span data-ttu-id="27b4a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b4a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b4a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b4a-129">-WhatIf</span></span>
<span data-ttu-id="27b4a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b4a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b4a-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="27b4a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b4a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b4a-132">CommonParameters</span></span>
<span data-ttu-id="27b4a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b4a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b4a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27b4a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b4a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27b4a-135">INPUTS</span></span>

### <span data-ttu-id="27b4a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="27b4a-136">System.String</span></span>

## <span data-ttu-id="27b4a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27b4a-137">OUTPUTS</span></span>

### <span data-ttu-id="27b4a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="27b4a-138">System.String</span></span>

## <span data-ttu-id="27b4a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27b4a-139">NOTES</span></span>

## <span data-ttu-id="27b4a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27b4a-140">RELATED LINKS</span></span>
