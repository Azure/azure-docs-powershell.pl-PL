---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184643"
---
# <span data-ttu-id="5402b-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="5402b-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="5402b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5402b-102">SYNOPSIS</span></span>
<span data-ttu-id="5402b-103">To polecenie commandlet pobiera zasoby połączeń, markę urządzenia VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracji, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach VPN.</span><span class="sxs-lookup"><span data-stu-id="5402b-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="5402b-104">Skrypt będzie postępować zgodnie ze składnią wybranego urządzenia i wypełnij niezbędne parametry, takie jak publiczne adresy IP bramy Azure, prefiksy wirtualnych adresów sieciowych, wstępnie udostępniony klucz podpowiązków VPN, itd., aby klienci mogą po prostu kopiować-wklejać do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="5402b-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="5402b-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5402b-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5402b-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="5402b-106">DESCRIPTION</span></span>
<span data-ttu-id="5402b-107">To polecenie commandlet pobiera zasoby połączeń, markę urządzenia VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracji, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach VPN.</span><span class="sxs-lookup"><span data-stu-id="5402b-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="5402b-108">Skrypt będzie postępować zgodnie ze składnią wybranego urządzenia i wypełnij niezbędne parametry, takie jak publiczne adresy IP bramy Azure, prefiksy wirtualnych adresów sieciowych, wstępnie udostępniony klucz podpowiązków VPN, itd., aby klienci mogą po prostu kopiować-wklejać do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="5402b-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="5402b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5402b-109">EXAMPLES</span></span>

### <span data-ttu-id="5402b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5402b-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="5402b-111">W powyższym przykładzie Get-AzVirtualNetworkGatewaySupportedVpnDevice do uzyskania obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego.</span><span class="sxs-lookup"><span data-stu-id="5402b-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="5402b-112">Następnie używa jednego z zwracanych modeli w celu wygenerowania skryptu konfiguracji urządzenia VPN dla funkcji VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="5402b-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="5402b-113">Urządzenie użyte w tym przykładzie ma deviceFamily "IOS-Test", DeviceVendor "Cisco-Test" i FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="5402b-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="5402b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5402b-114">PARAMETERS</span></span>

### <span data-ttu-id="5402b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5402b-115">-DefaultProfile</span></span>
<span data-ttu-id="5402b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5402b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5402b-117">— DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="5402b-117">-DeviceFamily</span></span>
<span data-ttu-id="5402b-118">Nazwa modelu/rodziny urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="5402b-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="5402b-119">- DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="5402b-119">-DeviceVendor</span></span>
<span data-ttu-id="5402b-120">Nazwa dostawcy urządzenia SIECI VPN.</span><span class="sxs-lookup"><span data-stu-id="5402b-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="5402b-121">- FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="5402b-121">-FirmwareVersion</span></span>
<span data-ttu-id="5402b-122">Wersja oprogramowania układowego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="5402b-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="5402b-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5402b-123">-Name</span></span>
<span data-ttu-id="5402b-124">Nazwa zasobu połączenia, dla którego ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="5402b-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="5402b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5402b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5402b-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5402b-126">The resource group name.</span></span>

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

### <span data-ttu-id="5402b-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5402b-127">-Confirm</span></span>
<span data-ttu-id="5402b-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5402b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5402b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5402b-129">-WhatIf</span></span>
<span data-ttu-id="5402b-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5402b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5402b-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5402b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5402b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5402b-132">CommonParameters</span></span>
<span data-ttu-id="5402b-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5402b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5402b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5402b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5402b-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5402b-135">INPUTS</span></span>

### <span data-ttu-id="5402b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5402b-136">System.String</span></span>

## <span data-ttu-id="5402b-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5402b-137">OUTPUTS</span></span>

### <span data-ttu-id="5402b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5402b-138">System.String</span></span>

## <span data-ttu-id="5402b-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5402b-139">NOTES</span></span>

## <span data-ttu-id="5402b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5402b-140">RELATED LINKS</span></span>
