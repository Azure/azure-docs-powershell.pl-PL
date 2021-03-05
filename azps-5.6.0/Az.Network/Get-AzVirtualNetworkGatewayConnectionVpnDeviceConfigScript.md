---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 967e45ce124ead583a7c2f3e36a80dedb80d4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978289"
---
# <span data-ttu-id="62e87-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="62e87-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="62e87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62e87-102">SYNOPSIS</span></span>
<span data-ttu-id="62e87-103">To polecenie commandlet pobiera zasoby połączeń, markę urządzenia VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracji, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach VPN.</span><span class="sxs-lookup"><span data-stu-id="62e87-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="62e87-104">Skrypt będzie postępować zgodnie ze składnią wybranego urządzenia i wypełnij niezbędne parametry, takie jak publiczne adresy IP bramy Azure, prefiksy wirtualnych adresów sieciowych, wstępnie udostępniony klucz podpowiązków VPN, itd., aby klienci mogą po prostu kopiować-wklejać do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="62e87-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="62e87-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62e87-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e87-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="62e87-106">DESCRIPTION</span></span>
<span data-ttu-id="62e87-107">To polecenie commandlet pobiera zasoby połączeń, markę urządzenia VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracji, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach VPN.</span><span class="sxs-lookup"><span data-stu-id="62e87-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="62e87-108">Skrypt będzie postępować zgodnie ze składnią wybranego urządzenia i wypełnij niezbędne parametry, takie jak publiczne adresy IP bramy Azure, prefiksy wirtualnych adresów sieciowych, wstępnie udostępniony klucz podpowiązków VPN, itd., aby klienci mogą po prostu kopiować-wklejać do swoich konfiguracji urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="62e87-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="62e87-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62e87-109">EXAMPLES</span></span>

### <span data-ttu-id="62e87-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62e87-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="62e87-111">W powyższym przykładzie Get-AzVirtualNetworkGatewaySupportedVpnDevice, aby uzyskać obsługiwane marki, modele i wersje oprogramowania układowego vpn.</span><span class="sxs-lookup"><span data-stu-id="62e87-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="62e87-112">Następnie używa jednego z zwracanych modeli w celu wygenerowania skryptu konfiguracji urządzenia VPN dla funkcji VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="62e87-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="62e87-113">Urządzenie użyte w tym przykładzie ma deviceFamily "IOS-Test", DeviceVendor "Cisco-Test" i FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="62e87-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="62e87-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62e87-114">PARAMETERS</span></span>

### <span data-ttu-id="62e87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e87-115">-DefaultProfile</span></span>
<span data-ttu-id="62e87-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62e87-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62e87-117">— DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="62e87-117">-DeviceFamily</span></span>
<span data-ttu-id="62e87-118">Nazwa modelu/rodziny urządzeń VPN.</span><span class="sxs-lookup"><span data-stu-id="62e87-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="62e87-119">- DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="62e87-119">-DeviceVendor</span></span>
<span data-ttu-id="62e87-120">Nazwa dostawcy urządzenia SIECI VPN.</span><span class="sxs-lookup"><span data-stu-id="62e87-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="62e87-121">- FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="62e87-121">-FirmwareVersion</span></span>
<span data-ttu-id="62e87-122">Wersja oprogramowania układowego urządzenia VPN.</span><span class="sxs-lookup"><span data-stu-id="62e87-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="62e87-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="62e87-123">-Name</span></span>
<span data-ttu-id="62e87-124">Nazwa zasobu połączenia, dla którego ma zostać wygenerowana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="62e87-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="62e87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e87-125">-ResourceGroupName</span></span>
<span data-ttu-id="62e87-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62e87-126">The resource group name.</span></span>

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

### <span data-ttu-id="62e87-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62e87-127">-Confirm</span></span>
<span data-ttu-id="62e87-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62e87-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e87-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e87-129">-WhatIf</span></span>
<span data-ttu-id="62e87-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62e87-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e87-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62e87-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e87-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e87-132">CommonParameters</span></span>
<span data-ttu-id="62e87-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e87-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e87-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62e87-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e87-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62e87-135">INPUTS</span></span>

### <span data-ttu-id="62e87-136">System.String</span><span class="sxs-lookup"><span data-stu-id="62e87-136">System.String</span></span>

## <span data-ttu-id="62e87-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62e87-137">OUTPUTS</span></span>

### <span data-ttu-id="62e87-138">System.String</span><span class="sxs-lookup"><span data-stu-id="62e87-138">System.String</span></span>

## <span data-ttu-id="62e87-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62e87-139">NOTES</span></span>

## <span data-ttu-id="62e87-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62e87-140">RELATED LINKS</span></span>
