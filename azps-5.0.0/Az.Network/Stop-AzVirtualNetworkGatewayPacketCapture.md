---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224908"
---
# <span data-ttu-id="a464c-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a464c-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="a464c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a464c-102">SYNOPSIS</span></span>
<span data-ttu-id="a464c-103">Zatrzymuje operację przechwytywania pakietu w wirtualnej bramie sieci.</span><span class="sxs-lookup"><span data-stu-id="a464c-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="a464c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a464c-104">SYNTAX</span></span>

### <span data-ttu-id="a464c-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a464c-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a464c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a464c-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a464c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a464c-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a464c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a464c-108">DESCRIPTION</span></span>
<span data-ttu-id="a464c-109">Zatrzymuje operację przechwytywania pakietu w wirtualnej bramie sieci i przekazuje wynik w podanym SasUrlie magazynu.</span><span class="sxs-lookup"><span data-stu-id="a464c-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="a464c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a464c-110">EXAMPLES</span></span>

### <span data-ttu-id="a464c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a464c-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

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

### <span data-ttu-id="a464c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a464c-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

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

## <span data-ttu-id="a464c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a464c-113">PARAMETERS</span></span>

### <span data-ttu-id="a464c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a464c-114">-AsJob</span></span>
<span data-ttu-id="a464c-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a464c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a464c-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a464c-116">-Confirm</span></span>
<span data-ttu-id="a464c-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a464c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a464c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a464c-118">-DefaultProfile</span></span>
<span data-ttu-id="a464c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a464c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a464c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a464c-120">-InputObject</span></span>
<span data-ttu-id="a464c-121">Obiekt bramy sieci wirtualnej, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a464c-121">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a464c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a464c-122">-Name</span></span>
<span data-ttu-id="a464c-123">Nazwa bramy sieci wirtualnej, w której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a464c-123">The virtual network gateway name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a464c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a464c-124">-ResourceGroupName</span></span>
<span data-ttu-id="a464c-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a464c-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a464c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a464c-126">-ResourceId</span></span>
<span data-ttu-id="a464c-127">Identyfikator zasobu platformy Azure VirtualNetworkGateway, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a464c-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a464c-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="a464c-128">-SasUrl</span></span>
<span data-ttu-id="a464c-129">Przechwytywanie pakietów URL SAS w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a464c-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="a464c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a464c-130">-WhatIf</span></span>
<span data-ttu-id="a464c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a464c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a464c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a464c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a464c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a464c-133">CommonParameters</span></span>
<span data-ttu-id="a464c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a464c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a464c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a464c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a464c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a464c-136">INPUTS</span></span>

### <span data-ttu-id="a464c-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a464c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a464c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a464c-138">System.String</span></span>

## <span data-ttu-id="a464c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a464c-139">OUTPUTS</span></span>

### <span data-ttu-id="a464c-140">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a464c-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a464c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a464c-141">NOTES</span></span>

## <span data-ttu-id="a464c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a464c-142">RELATED LINKS</span></span>
[<span data-ttu-id="a464c-143">Start — AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a464c-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
