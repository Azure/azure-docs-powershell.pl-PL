---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: 1fa868d9df41a5f4f995981c332497d9555e1174
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219763"
---
# <span data-ttu-id="11eef-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="11eef-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="11eef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11eef-102">SYNOPSIS</span></span>
<span data-ttu-id="11eef-103">Pobiera informacje na temat dostępnych urządzeń brzegowych stosu.</span><span class="sxs-lookup"><span data-stu-id="11eef-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="11eef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11eef-104">SYNTAX</span></span>

### <span data-ttu-id="11eef-105">ListByParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11eef-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11eef-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11eef-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11eef-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11eef-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11eef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="11eef-108">DESCRIPTION</span></span>
<span data-ttu-id="11eef-109">Polecenie cmdlet **Get-AzStackEdgeDevice** pobiera informacje na temat dostępnych urządzeń brzegowych.</span><span class="sxs-lookup"><span data-stu-id="11eef-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="11eef-110">Możesz określić nazwę urządzenia wraz z nazwą grupy zasobów, aby uzyskać informacje na określonym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="11eef-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="11eef-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11eef-111">EXAMPLES</span></span>

### <span data-ttu-id="11eef-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11eef-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="11eef-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11eef-113">Example 2</span></span>
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

## <span data-ttu-id="11eef-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11eef-114">PARAMETERS</span></span>

### <span data-ttu-id="11eef-115">-Alert</span><span class="sxs-lookup"><span data-stu-id="11eef-115">-Alert</span></span>
<span data-ttu-id="11eef-116">Pobieranie alertów na urządzeniu z krawędzią/bramą stosu</span><span class="sxs-lookup"><span data-stu-id="11eef-116">Fetch the alerts on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="11eef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11eef-117">-DefaultProfile</span></span>
<span data-ttu-id="11eef-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11eef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11eef-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="11eef-119">-ExtendedInfo</span></span>
<span data-ttu-id="11eef-120">Pobiera dodatkowe informacje dla określonego urządzenia bramy z krawędzią/stosem.</span><span class="sxs-lookup"><span data-stu-id="11eef-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

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

### <span data-ttu-id="11eef-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11eef-121">-Name</span></span>
<span data-ttu-id="11eef-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="11eef-122">Resource Group Name</span></span>

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

### <span data-ttu-id="11eef-123">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="11eef-123">-NetworkSetting</span></span>
<span data-ttu-id="11eef-124">Pobiera ustawienia sieciowe określonego urządzenia bramy z krawędzią/stosem.</span><span class="sxs-lookup"><span data-stu-id="11eef-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

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

### <span data-ttu-id="11eef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11eef-125">-ResourceGroupName</span></span>
<span data-ttu-id="11eef-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="11eef-126">Resource Group Name</span></span>

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

### <span data-ttu-id="11eef-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11eef-127">-ResourceId</span></span>
<span data-ttu-id="11eef-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="11eef-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="11eef-129">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="11eef-129">-UpdateSummary</span></span>
<span data-ttu-id="11eef-130">Pobiera informacje o dostępności aktualizacji w oparciu o ostatnie skanowanie urządzenia.</span><span class="sxs-lookup"><span data-stu-id="11eef-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="11eef-131">Pobiera również informacje o wszystkich trwających zadaniach pobierania lub instalowania na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="11eef-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="11eef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11eef-132">CommonParameters</span></span>
<span data-ttu-id="11eef-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11eef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11eef-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11eef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11eef-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11eef-135">INPUTS</span></span>

## <span data-ttu-id="11eef-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11eef-136">OUTPUTS</span></span>

## <span data-ttu-id="11eef-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11eef-137">NOTES</span></span>

## <span data-ttu-id="11eef-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11eef-138">RELATED LINKS</span></span>
