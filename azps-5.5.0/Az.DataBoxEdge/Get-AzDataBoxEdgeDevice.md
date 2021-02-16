---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238409"
---
# <span data-ttu-id="974c6-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="974c6-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="974c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="974c6-102">SYNOPSIS</span></span>
<span data-ttu-id="974c6-103">Pobiera informacje na dostępnych urządzeniach Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="974c6-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="974c6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="974c6-104">SYNTAX</span></span>

### <span data-ttu-id="974c6-105">ListByParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="974c6-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="974c6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="974c6-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="974c6-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="974c6-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="974c6-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="974c6-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="974c6-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="974c6-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="974c6-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="974c6-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="974c6-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="974c6-116">OPIS</span><span class="sxs-lookup"><span data-stu-id="974c6-116">DESCRIPTION</span></span>
<span data-ttu-id="974c6-117">Polecenie **cmdlet Get-AzDataBoxEdgeDevice** pobiera informacje o dostępnych urządzeniach brzegowych pola danych.</span><span class="sxs-lookup"><span data-stu-id="974c6-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="974c6-118">Możesz określić nazwę urządzenia wraz z nazwą grupy zasobów, aby uzyskać informacje na określonym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="974c6-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="974c6-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="974c6-119">EXAMPLES</span></span>

### <span data-ttu-id="974c6-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="974c6-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="974c6-121">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="974c6-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="974c6-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="974c6-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="974c6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="974c6-123">PARAMETERS</span></span>

### <span data-ttu-id="974c6-124">— Alert</span><span class="sxs-lookup"><span data-stu-id="974c6-124">-Alert</span></span>
<span data-ttu-id="974c6-125">Pobieranie alertów na urządzeniu z krawędzią/bramą pola danych</span><span class="sxs-lookup"><span data-stu-id="974c6-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974c6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974c6-126">-DefaultProfile</span></span>
<span data-ttu-id="974c6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="974c6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="974c6-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="974c6-128">-ExtendedInfo</span></span>
<span data-ttu-id="974c6-129">Pobiera dodatkowe informacje dla określonego urządzenia edge/bramy pola danych</span><span class="sxs-lookup"><span data-stu-id="974c6-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974c6-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="974c6-130">-Name</span></span>
<span data-ttu-id="974c6-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="974c6-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974c6-132">— NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="974c6-132">-NetworkSetting</span></span>
<span data-ttu-id="974c6-133">Pobiera ustawienia sieciowe określonego urządzenia z bramą krawędzi pola danych/pola danych.</span><span class="sxs-lookup"><span data-stu-id="974c6-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974c6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="974c6-134">-ResourceGroupName</span></span>
<span data-ttu-id="974c6-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="974c6-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974c6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="974c6-136">-ResourceId</span></span>
<span data-ttu-id="974c6-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="974c6-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974c6-138">- UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="974c6-138">-UpdateSummary</span></span>
<span data-ttu-id="974c6-139">Informacje o dostępności aktualizacji są dostępne na podstawie ostatniego skanu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="974c6-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="974c6-140">Ponadto otrzymuje informacje o wszelkich trwających zadaniach pobierania lub instalowania na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="974c6-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974c6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974c6-141">CommonParameters</span></span>
<span data-ttu-id="974c6-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="974c6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974c6-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="974c6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974c6-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="974c6-144">INPUTS</span></span>

### <span data-ttu-id="974c6-145">Brak</span><span class="sxs-lookup"><span data-stu-id="974c6-145">None</span></span>

## <span data-ttu-id="974c6-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="974c6-146">OUTPUTS</span></span>

### <span data-ttu-id="974c6-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="974c6-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="974c6-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="974c6-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="974c6-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="974c6-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="974c6-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="974c6-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="974c6-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="974c6-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="974c6-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="974c6-152">NOTES</span></span>

## <span data-ttu-id="974c6-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="974c6-153">RELATED LINKS</span></span>
