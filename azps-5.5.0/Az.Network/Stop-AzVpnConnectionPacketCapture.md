---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: f80543b245c59cee7261d062c741788489fb5cb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240514"
---
# <span data-ttu-id="69a0b-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69a0b-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="69a0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="69a0b-103">Zatrzymuje operację przechwytywania pakietów przy połączeniu Vpn</span><span class="sxs-lookup"><span data-stu-id="69a0b-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="69a0b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69a0b-104">SYNTAX</span></span>

### <span data-ttu-id="69a0b-105">ByVpnConnectionName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="69a0b-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a0b-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="69a0b-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a0b-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="69a0b-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69a0b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="69a0b-108">DESCRIPTION</span></span>
<span data-ttu-id="69a0b-109">Zatrzymuje operację przechwytywania pakietów na połączeniu vpn i przekaże wynik na danym pliku SasUrl kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="69a0b-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="69a0b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69a0b-110">EXAMPLES</span></span>

### <span data-ttu-id="69a0b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69a0b-111">Example 1</span></span>
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

### <span data-ttu-id="69a0b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="69a0b-112">Example 2</span></span>
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

## <span data-ttu-id="69a0b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69a0b-113">PARAMETERS</span></span>

### <span data-ttu-id="69a0b-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="69a0b-114">-AsJob</span></span>
<span data-ttu-id="69a0b-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="69a0b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69a0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a0b-116">-DefaultProfile</span></span>
<span data-ttu-id="69a0b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69a0b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69a0b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69a0b-118">-InputObject</span></span>
<span data-ttu-id="69a0b-119">Obiekt połączenia Vpn, w którym ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="69a0b-119">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="69a0b-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="69a0b-120">-LinkConnectionName</span></span>
<span data-ttu-id="69a0b-121">Nazwy witryny SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="69a0b-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="69a0b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69a0b-122">-Name</span></span>
<span data-ttu-id="69a0b-123">Nazwa połączenia VPN, na którym ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="69a0b-123">The Vpn connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="69a0b-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="69a0b-124">-ParentResourceName</span></span>
<span data-ttu-id="69a0b-125">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="69a0b-125">The parent resource name.</span></span>

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

### <span data-ttu-id="69a0b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69a0b-126">-ResourceGroupName</span></span>
<span data-ttu-id="69a0b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69a0b-127">The resource group name.</span></span>

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

### <span data-ttu-id="69a0b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69a0b-128">-ResourceId</span></span>
<span data-ttu-id="69a0b-129">Identyfikator zasobu Azure połączenia VpnConnection, w którym ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="69a0b-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="69a0b-130">- SasUrl</span><span class="sxs-lookup"><span data-stu-id="69a0b-130">-SasUrl</span></span>
<span data-ttu-id="69a0b-131">Adres URL sas do zatrzymania przechwytywania pakietów w sieci Vpn.</span><span class="sxs-lookup"><span data-stu-id="69a0b-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="69a0b-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69a0b-132">-Confirm</span></span>
<span data-ttu-id="69a0b-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69a0b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a0b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a0b-134">-WhatIf</span></span>
<span data-ttu-id="69a0b-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69a0b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a0b-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69a0b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69a0b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a0b-137">CommonParameters</span></span>
<span data-ttu-id="69a0b-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a0b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a0b-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69a0b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a0b-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69a0b-140">INPUTS</span></span>

### <span data-ttu-id="69a0b-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="69a0b-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="69a0b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="69a0b-142">System.String</span></span>

## <span data-ttu-id="69a0b-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69a0b-143">OUTPUTS</span></span>

### <span data-ttu-id="69a0b-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="69a0b-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="69a0b-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69a0b-145">NOTES</span></span>

## <span data-ttu-id="69a0b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69a0b-146">RELATED LINKS</span></span>

[<span data-ttu-id="69a0b-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69a0b-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)