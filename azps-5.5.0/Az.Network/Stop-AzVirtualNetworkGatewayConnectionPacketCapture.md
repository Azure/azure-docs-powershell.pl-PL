---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240531"
---
# <span data-ttu-id="a8034-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8034-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="a8034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8034-102">SYNOPSIS</span></span>
<span data-ttu-id="a8034-103">Zatrzymuje operację przechwytywania pakietów dla połączenia wirtualnej bramy sieciowej</span><span class="sxs-lookup"><span data-stu-id="a8034-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="a8034-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8034-104">SYNTAX</span></span>

### <span data-ttu-id="a8034-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="a8034-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8034-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a8034-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8034-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8034-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8034-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8034-108">DESCRIPTION</span></span>
<span data-ttu-id="a8034-109">Zatrzymuje operację przechwytywania pakietów dla połączenia wirtualnej bramy sieciowej i przekaże wynik dla danego sasurl kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="a8034-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="a8034-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8034-110">EXAMPLES</span></span>

### <span data-ttu-id="a8034-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8034-111">Example 1</span></span>
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

### <span data-ttu-id="a8034-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a8034-112">Example 2</span></span>
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

## <span data-ttu-id="a8034-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8034-113">PARAMETERS</span></span>

### <span data-ttu-id="a8034-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a8034-114">-AsJob</span></span>
<span data-ttu-id="a8034-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a8034-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8034-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8034-116">-Confirm</span></span>
<span data-ttu-id="a8034-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a8034-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8034-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8034-118">-DefaultProfile</span></span>
<span data-ttu-id="a8034-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8034-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8034-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8034-120">-InputObject</span></span>
<span data-ttu-id="a8034-121">Obiekt połączenia wirtualnej bramy sieciowej, w którym ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a8034-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="a8034-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a8034-122">-Name</span></span>
<span data-ttu-id="a8034-123">Nazwa połączenia wirtualnej bramy sieciowej, na której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a8034-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="a8034-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8034-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8034-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8034-125">The resource group name.</span></span>

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

### <span data-ttu-id="a8034-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8034-126">-ResourceId</span></span>
<span data-ttu-id="a8034-127">Identyfikator zasobu Azure w usłudze VirtualNetworkGatewayConnection, w którym ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a8034-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="a8034-128">- SasUrl</span><span class="sxs-lookup"><span data-stu-id="a8034-128">-SasUrl</span></span>
<span data-ttu-id="a8034-129">Adres URL sas do zatrzymania przechwytywania pakietów w wirtualnej bramie sieciowej.</span><span class="sxs-lookup"><span data-stu-id="a8034-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="a8034-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8034-130">-WhatIf</span></span>
<span data-ttu-id="a8034-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8034-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8034-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a8034-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8034-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8034-133">CommonParameters</span></span>
<span data-ttu-id="a8034-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8034-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8034-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8034-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8034-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8034-136">INPUTS</span></span>

### <span data-ttu-id="a8034-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a8034-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="a8034-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a8034-138">System.String</span></span>

## <span data-ttu-id="a8034-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8034-139">OUTPUTS</span></span>

### <span data-ttu-id="a8034-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a8034-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a8034-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8034-141">NOTES</span></span>

## <span data-ttu-id="a8034-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8034-142">RELATED LINKS</span></span>
[<span data-ttu-id="a8034-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8034-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)