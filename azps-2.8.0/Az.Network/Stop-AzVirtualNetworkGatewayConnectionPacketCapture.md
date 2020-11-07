---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 791b6d74049aeec24e67ca29f5fae990f511908d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872080"
---
# <span data-ttu-id="1e831-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e831-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="1e831-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e831-102">SYNOPSIS</span></span>
<span data-ttu-id="1e831-103">Zatrzymuje operację przechwytywania pakietów w połączeniu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1e831-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="1e831-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e831-104">SYNTAX</span></span>

### <span data-ttu-id="1e831-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e831-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e831-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e831-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e831-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e831-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e831-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1e831-108">DESCRIPTION</span></span>
<span data-ttu-id="1e831-109">Zatrzymuje operację przechwytywania pakietów w połączeniu bramy sieci wirtualnej i przekazuje wynik w podanym SasUrlie magazynu.</span><span class="sxs-lookup"><span data-stu-id="1e831-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="1e831-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e831-110">EXAMPLES</span></span>

### <span data-ttu-id="1e831-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e831-111">Example 1</span></span>
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

### <span data-ttu-id="1e831-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1e831-112">Example 2</span></span>
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

## <span data-ttu-id="1e831-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e831-113">PARAMETERS</span></span>

### <span data-ttu-id="1e831-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e831-114">-AsJob</span></span>
<span data-ttu-id="1e831-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1e831-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e831-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e831-116">-Confirm</span></span>
<span data-ttu-id="1e831-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e831-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e831-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e831-118">-DefaultProfile</span></span>
<span data-ttu-id="1e831-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e831-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e831-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1e831-120">-InputObject</span></span>
<span data-ttu-id="1e831-121">Obiekt połączenie bramy sieci wirtualnej, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="1e831-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="1e831-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e831-122">-Name</span></span>
<span data-ttu-id="1e831-123">Nazwa połączenia bramy sieci wirtualnej, w której ma zostać uruchomione przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="1e831-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="1e831-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e831-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e831-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e831-125">The resource group name.</span></span>

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

### <span data-ttu-id="1e831-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e831-126">-ResourceId</span></span>
<span data-ttu-id="1e831-127">Identyfikator zasobu platformy Azure VirtualNetworkGatewayConnection, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="1e831-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="1e831-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="1e831-128">-SasUrl</span></span>
<span data-ttu-id="1e831-129">Adres URL SAS na potrzeby funkcji przechwytywania pakietów w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1e831-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="1e831-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e831-130">-WhatIf</span></span>
<span data-ttu-id="1e831-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e831-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e831-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1e831-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e831-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e831-133">CommonParameters</span></span>
<span data-ttu-id="1e831-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e831-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e831-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e831-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e831-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e831-136">INPUTS</span></span>

### <span data-ttu-id="1e831-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1e831-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="1e831-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1e831-138">System.String</span></span>

## <span data-ttu-id="1e831-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e831-139">OUTPUTS</span></span>

### <span data-ttu-id="1e831-140">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="1e831-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="1e831-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e831-141">NOTES</span></span>

## <span data-ttu-id="1e831-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e831-142">RELATED LINKS</span></span>
[<span data-ttu-id="1e831-143">Start — AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e831-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)