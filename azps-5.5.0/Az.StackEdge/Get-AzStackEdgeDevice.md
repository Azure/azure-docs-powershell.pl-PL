---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: 1fa868d9df41a5f4f995981c332497d9555e1174
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188907"
---
# <span data-ttu-id="140cc-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="140cc-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="140cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="140cc-102">SYNOPSIS</span></span>
<span data-ttu-id="140cc-103">Pobiera informacje na dostępnych urządzeniach Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="140cc-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="140cc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="140cc-104">SYNTAX</span></span>

### <span data-ttu-id="140cc-105">ListByParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="140cc-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="140cc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="140cc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="140cc-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="140cc-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="140cc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="140cc-108">DESCRIPTION</span></span>
<span data-ttu-id="140cc-109">Polecenie **cmdlet Get-AzStackEdgeDevice** pobiera informacje o dostępnych urządzeniach Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="140cc-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="140cc-110">Możesz określić nazwę urządzenia wraz z nazwą grupy zasobów, aby uzyskać informacje na określonym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="140cc-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="140cc-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="140cc-111">EXAMPLES</span></span>

### <span data-ttu-id="140cc-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="140cc-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="140cc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="140cc-113">Example 2</span></span>
```powershell
PS C:\>$device = Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName1 -DeviceName deviceNameOne -Alert -UpdateSummary -NetworkSetting -ExtendedInfo

PS C:\>$device.Alert

Title                            Severity AppearedDateTime      Recommendation
-----                            -------- ----------------      --------------
Lost heartbeat from your device. Critical 02-Jan-20 10:35:20 AM If your device is offline, then the device is not able to communicate with the Azure service. This could be due to one of the following reasons: <br/> &nbs�


PS C:\>$device.NetworkSetting

State    IPv4         IPv6                                 Subnet        Default Gateway Physical address DNS Servers
-----    ----         ----                                 ------        --------------- ---------------- -----------
Disabled 10.150.76.82 2404:f801:4800:1e:8168:dca6:b3b9:d70 255.255.252.0 10.150.76.1     00155D4E262B     10.50.50.50,10.50.10.50

PS C:\>$device.UpdateSummary

DeviceName        Current Version Friendly name      Last Software Scan Last Software Update Pending Updates Pending Update Titles
----------        --------------- -------------      ------------------ -------------------- --------------- ---------------------
deviceNameOne     2.0.998.537     Data Box Edge Mock                                         0

PS C:\>$device.ExtendedInfo

ResourceGroupName   DeviceName        EncryptedCIK Thumbprint     ResourceKey        EncryptedCIK
-----------------   ----------        -----------------------     -----------        ------------
resourceGroupName1  deviceNameOne     EncryptedCIKThumbpring      411182691329779166 EncryptedCIK
```

## <span data-ttu-id="140cc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="140cc-114">PARAMETERS</span></span>

### <span data-ttu-id="140cc-115">— Alert</span><span class="sxs-lookup"><span data-stu-id="140cc-115">-Alert</span></span>
<span data-ttu-id="140cc-116">Pobieranie alertów na urządzeniu krawędź/brama stosu</span><span class="sxs-lookup"><span data-stu-id="140cc-116">Fetch the alerts on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140cc-117">-DefaultProfile</span></span>
<span data-ttu-id="140cc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="140cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="140cc-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="140cc-119">-ExtendedInfo</span></span>
<span data-ttu-id="140cc-120">Pobiera dodatkowe informacje dla określonego urządzenia Stack Edge/Stack Gateway</span><span class="sxs-lookup"><span data-stu-id="140cc-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140cc-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="140cc-121">-Name</span></span>
<span data-ttu-id="140cc-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="140cc-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140cc-123">— NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="140cc-123">-NetworkSetting</span></span>
<span data-ttu-id="140cc-124">Pobiera ustawienia sieciowe określonego urządzenia Stack Edge/Stack Gateway.</span><span class="sxs-lookup"><span data-stu-id="140cc-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="140cc-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="140cc-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140cc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="140cc-127">-ResourceId</span></span>
<span data-ttu-id="140cc-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="140cc-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140cc-129">- UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="140cc-129">-UpdateSummary</span></span>
<span data-ttu-id="140cc-130">Informacje o dostępności aktualizacji są dostępne na podstawie ostatniego skanu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="140cc-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="140cc-131">Ponadto otrzymuje informacje o wszelkich trwających zadaniach pobierania lub instalowania na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="140cc-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140cc-132">CommonParameters</span></span>
<span data-ttu-id="140cc-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="140cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140cc-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="140cc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140cc-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="140cc-135">INPUTS</span></span>

## <span data-ttu-id="140cc-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="140cc-136">OUTPUTS</span></span>

## <span data-ttu-id="140cc-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="140cc-137">NOTES</span></span>

## <span data-ttu-id="140cc-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="140cc-138">RELATED LINKS</span></span>
