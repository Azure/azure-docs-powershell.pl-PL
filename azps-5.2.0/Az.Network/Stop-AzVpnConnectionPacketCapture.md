---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: f80543b245c59cee7261d062c741788489fb5cb7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363405"
---
# <span data-ttu-id="414ef-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="414ef-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="414ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="414ef-102">SYNOPSIS</span></span>
<span data-ttu-id="414ef-103">Zatrzymuje operację przechwytywania pakietów w połączeniu VPN</span><span class="sxs-lookup"><span data-stu-id="414ef-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="414ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="414ef-104">SYNTAX</span></span>

### <span data-ttu-id="414ef-105">ByVpnConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="414ef-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="414ef-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="414ef-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="414ef-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="414ef-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="414ef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="414ef-108">DESCRIPTION</span></span>
<span data-ttu-id="414ef-109">Zatrzymuje operację przechwytywania pakietów w połączeniu sieci VPN i przekazuje wynik w podanym SasUrlie magazynu.</span><span class="sxs-lookup"><span data-stu-id="414ef-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="414ef-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="414ef-110">EXAMPLES</span></span>

### <span data-ttu-id="414ef-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="414ef-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="414ef-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="414ef-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="414ef-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="414ef-113">PARAMETERS</span></span>

### <span data-ttu-id="414ef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="414ef-114">-AsJob</span></span>
<span data-ttu-id="414ef-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="414ef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="414ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414ef-116">-DefaultProfile</span></span>
<span data-ttu-id="414ef-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="414ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="414ef-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="414ef-118">-InputObject</span></span>
<span data-ttu-id="414ef-119">Obiekt połączenia VPN, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="414ef-119">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="414ef-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="414ef-120">-LinkConnectionName</span></span>
<span data-ttu-id="414ef-121">Nazwy SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="414ef-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="414ef-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="414ef-122">-Name</span></span>
<span data-ttu-id="414ef-123">Nazwa połączenia z siecią VPN, w którym ma zostać uruchomione przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="414ef-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414ef-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="414ef-124">-ParentResourceName</span></span>
<span data-ttu-id="414ef-125">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="414ef-125">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="414ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="414ef-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="414ef-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414ef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="414ef-128">-ResourceId</span></span>
<span data-ttu-id="414ef-129">Identyfikator zasobu platformy Azure VpnConnection, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="414ef-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414ef-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="414ef-130">-SasUrl</span></span>
<span data-ttu-id="414ef-131">Adres URL SAS na potrzeby zatrzymywania przechwytywania pakietów w sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="414ef-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="414ef-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="414ef-132">-Confirm</span></span>
<span data-ttu-id="414ef-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="414ef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414ef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414ef-134">-WhatIf</span></span>
<span data-ttu-id="414ef-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="414ef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="414ef-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="414ef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="414ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414ef-137">CommonParameters</span></span>
<span data-ttu-id="414ef-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="414ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414ef-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="414ef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414ef-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="414ef-140">INPUTS</span></span>

### <span data-ttu-id="414ef-141">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="414ef-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="414ef-142">System. String</span><span class="sxs-lookup"><span data-stu-id="414ef-142">System.String</span></span>

## <span data-ttu-id="414ef-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="414ef-143">OUTPUTS</span></span>

### <span data-ttu-id="414ef-144">Microsoft. Azure. Commands. Network. models. PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="414ef-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="414ef-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="414ef-145">NOTES</span></span>

## <span data-ttu-id="414ef-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="414ef-146">RELATED LINKS</span></span>

[<span data-ttu-id="414ef-147">Start — AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="414ef-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)