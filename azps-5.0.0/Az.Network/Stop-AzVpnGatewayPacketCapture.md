---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318540"
---
# <span data-ttu-id="cc5a9-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc5a9-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="cc5a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5a9-103">Zatrzymuje operację przechwytywania pakietów na bramie VPN.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="cc5a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc5a9-104">SYNTAX</span></span>

### <span data-ttu-id="cc5a9-105">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc5a9-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5a9-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cc5a9-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5a9-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cc5a9-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc5a9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cc5a9-108">DESCRIPTION</span></span>
<span data-ttu-id="cc5a9-109">Zatrzymuje operację przechwytywania pakietu na bramie VPN i przekazuje wynik w podanym SasUrlu magazynu.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="cc5a9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc5a9-110">EXAMPLES</span></span>

### <span data-ttu-id="cc5a9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc5a9-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="cc5a9-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cc5a9-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="cc5a9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc5a9-113">PARAMETERS</span></span>

### <span data-ttu-id="cc5a9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc5a9-114">-AsJob</span></span>
<span data-ttu-id="cc5a9-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cc5a9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc5a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5a9-116">-DefaultProfile</span></span>
<span data-ttu-id="cc5a9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc5a9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc5a9-118">-InputObject</span></span>
<span data-ttu-id="cc5a9-119">Obiekt bramy sieci VPN, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-119">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5a9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc5a9-120">-Name</span></span>
<span data-ttu-id="cc5a9-121">Nazwa bramy sieci VPN, w której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-121">The Vpn Gateway name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc5a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc5a9-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5a9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc5a9-124">-ResourceId</span></span>
<span data-ttu-id="cc5a9-125">Identyfikator zasobu platformy Azure VpnGateway, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5a9-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="cc5a9-126">-SasUrl</span></span>
<span data-ttu-id="cc5a9-127">Przechwytywanie pakietów przez adres URL SAS w bramie VPN.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-127">SAS URL packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5a9-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc5a9-128">-Confirm</span></span>
<span data-ttu-id="cc5a9-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc5a9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc5a9-130">-WhatIf</span></span>
<span data-ttu-id="cc5a9-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc5a9-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc5a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5a9-133">CommonParameters</span></span>
<span data-ttu-id="cc5a9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc5a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5a9-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc5a9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5a9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc5a9-136">INPUTS</span></span>

### <span data-ttu-id="cc5a9-137">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cc5a9-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="cc5a9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cc5a9-138">System.String</span></span>

## <span data-ttu-id="cc5a9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc5a9-139">OUTPUTS</span></span>

### <span data-ttu-id="cc5a9-140">Microsoft. Azure. Commands. Network. models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="cc5a9-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="cc5a9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc5a9-141">NOTES</span></span>

## <span data-ttu-id="cc5a9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc5a9-142">RELATED LINKS</span></span>

[<span data-ttu-id="cc5a9-143">Start — AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc5a9-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)