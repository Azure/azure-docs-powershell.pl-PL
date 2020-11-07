---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 39bb650333c59bd7d7185449025de7bdd6254fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872076"
---
# <span data-ttu-id="a2ed6-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2ed6-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="a2ed6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ed6-103">Zatrzymuje operację przechwytywania pakietu w wirtualnej bramie sieci.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="a2ed6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2ed6-104">SYNTAX</span></span>

### <span data-ttu-id="a2ed6-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2ed6-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ed6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2ed6-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ed6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2ed6-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2ed6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a2ed6-108">DESCRIPTION</span></span>
<span data-ttu-id="a2ed6-109">Zatrzymuje operację przechwytywania pakietu w wirtualnej bramie sieci i przekazuje wynik w podanym SasUrlie magazynu.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="a2ed6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2ed6-110">EXAMPLES</span></span>

### <span data-ttu-id="a2ed6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2ed6-111">Example 1</span></span>
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

### <span data-ttu-id="a2ed6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a2ed6-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
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

## <span data-ttu-id="a2ed6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2ed6-113">PARAMETERS</span></span>

### <span data-ttu-id="a2ed6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2ed6-114">-AsJob</span></span>
<span data-ttu-id="a2ed6-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a2ed6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2ed6-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2ed6-116">-Confirm</span></span>
<span data-ttu-id="a2ed6-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2ed6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ed6-118">-DefaultProfile</span></span>
<span data-ttu-id="a2ed6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2ed6-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a2ed6-120">-InputObject</span></span>
<span data-ttu-id="a2ed6-121">Obiekt bramy sieci wirtualnej, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="a2ed6-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a2ed6-122">-Name</span></span>
<span data-ttu-id="a2ed6-123">Nazwa bramy sieci wirtualnej, w której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="a2ed6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ed6-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2ed6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-125">The resource group name.</span></span>

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

### <span data-ttu-id="a2ed6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2ed6-126">-ResourceId</span></span>
<span data-ttu-id="a2ed6-127">Identyfikator zasobu platformy Azure VirtualNetworkGateway, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="a2ed6-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="a2ed6-128">-SasUrl</span></span>
<span data-ttu-id="a2ed6-129">Przechwytywanie pakietów URL SAS w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="a2ed6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ed6-130">-WhatIf</span></span>
<span data-ttu-id="a2ed6-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2ed6-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2ed6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ed6-133">CommonParameters</span></span>
<span data-ttu-id="a2ed6-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ed6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ed6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2ed6-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ed6-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2ed6-136">INPUTS</span></span>

### <span data-ttu-id="a2ed6-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2ed6-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a2ed6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a2ed6-138">System.String</span></span>

## <span data-ttu-id="a2ed6-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2ed6-139">OUTPUTS</span></span>

### <span data-ttu-id="a2ed6-140">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a2ed6-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a2ed6-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2ed6-141">NOTES</span></span>

## <span data-ttu-id="a2ed6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2ed6-142">RELATED LINKS</span></span>
[<span data-ttu-id="a2ed6-143">Start — AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2ed6-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)