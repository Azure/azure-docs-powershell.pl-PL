---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219362"
---
# <span data-ttu-id="7fa02-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7fa02-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="7fa02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fa02-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa02-103">Zatrzymuje operację przechwytywania pakietów w połączeniu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7fa02-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="7fa02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fa02-104">SYNTAX</span></span>

### <span data-ttu-id="7fa02-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7fa02-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa02-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7fa02-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa02-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7fa02-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fa02-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7fa02-108">DESCRIPTION</span></span>
<span data-ttu-id="7fa02-109">Zatrzymuje operację przechwytywania pakietów w połączeniu bramy sieci wirtualnej i przekazuje wynik w podanym SasUrlie magazynu.</span><span class="sxs-lookup"><span data-stu-id="7fa02-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="7fa02-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fa02-110">EXAMPLES</span></span>

### <span data-ttu-id="7fa02-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7fa02-111">Example 1</span></span>
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
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="7fa02-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7fa02-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="7fa02-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fa02-113">PARAMETERS</span></span>

### <span data-ttu-id="7fa02-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fa02-114">-AsJob</span></span>
<span data-ttu-id="7fa02-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7fa02-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fa02-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7fa02-116">-Confirm</span></span>
<span data-ttu-id="7fa02-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fa02-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fa02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa02-118">-DefaultProfile</span></span>
<span data-ttu-id="7fa02-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fa02-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fa02-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7fa02-120">-InputObject</span></span>
<span data-ttu-id="7fa02-121">Obiekt połączenie bramy sieci wirtualnej, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="7fa02-121">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fa02-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7fa02-122">-Name</span></span>
<span data-ttu-id="7fa02-123">Nazwa połączenia bramy sieci wirtualnej, w której ma zostać uruchomione przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="7fa02-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa02-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fa02-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7fa02-125">The resource group name.</span></span>

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

### <span data-ttu-id="7fa02-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fa02-126">-ResourceId</span></span>
<span data-ttu-id="7fa02-127">Identyfikator zasobu platformy Azure VirtualNetworkGatewayConnection, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="7fa02-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="7fa02-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="7fa02-128">-SasUrl</span></span>
<span data-ttu-id="7fa02-129">Adres URL SAS na potrzeby funkcji przechwytywania pakietów w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7fa02-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="7fa02-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fa02-130">-WhatIf</span></span>
<span data-ttu-id="7fa02-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fa02-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fa02-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7fa02-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fa02-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa02-133">CommonParameters</span></span>
<span data-ttu-id="7fa02-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa02-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa02-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fa02-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa02-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fa02-136">INPUTS</span></span>

### <span data-ttu-id="7fa02-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7fa02-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="7fa02-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7fa02-138">System.String</span></span>

## <span data-ttu-id="7fa02-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fa02-139">OUTPUTS</span></span>

### <span data-ttu-id="7fa02-140">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="7fa02-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="7fa02-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fa02-141">NOTES</span></span>

## <span data-ttu-id="7fa02-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fa02-142">RELATED LINKS</span></span>
[<span data-ttu-id="7fa02-143">Start — AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7fa02-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)