---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330358"
---
# <span data-ttu-id="da5d5-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="da5d5-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="da5d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="da5d5-103">Pobiera informacje na temat dostępnych urządzeń z krawędziami pola danych.</span><span class="sxs-lookup"><span data-stu-id="da5d5-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="da5d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da5d5-104">SYNTAX</span></span>

### <span data-ttu-id="da5d5-105">ListByParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da5d5-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da5d5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5d5-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da5d5-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da5d5-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da5d5-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da5d5-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5d5-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5d5-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5d5-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5d5-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="da5d5-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da5d5-116">Opis</span><span class="sxs-lookup"><span data-stu-id="da5d5-116">DESCRIPTION</span></span>
<span data-ttu-id="da5d5-117">Polecenie cmdlet **Get-AzDataBoxEdgeDevice** pobiera informacje o dostępnych urządzeniach z krawędziami pola danych.</span><span class="sxs-lookup"><span data-stu-id="da5d5-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="da5d5-118">Możesz określić nazwę urządzenia wraz z nazwą grupy zasobów, aby uzyskać informacje na określonym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="da5d5-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="da5d5-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da5d5-119">EXAMPLES</span></span>

### <span data-ttu-id="da5d5-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da5d5-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="da5d5-121">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="da5d5-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="da5d5-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="da5d5-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="da5d5-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da5d5-123">PARAMETERS</span></span>

### <span data-ttu-id="da5d5-124">-Alert</span><span class="sxs-lookup"><span data-stu-id="da5d5-124">-Alert</span></span>
<span data-ttu-id="da5d5-125">Pobieranie alertów na urządzeniu z krawędzią/bramą pola danych</span><span class="sxs-lookup"><span data-stu-id="da5d5-125">Fetch the alerts on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="da5d5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5d5-126">-DefaultProfile</span></span>
<span data-ttu-id="da5d5-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da5d5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da5d5-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="da5d5-128">-ExtendedInfo</span></span>
<span data-ttu-id="da5d5-129">Pobiera dodatkowe informacje dla określonego pola danych krawędź/Brama pola danych.</span><span class="sxs-lookup"><span data-stu-id="da5d5-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="da5d5-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da5d5-130">-Name</span></span>
<span data-ttu-id="da5d5-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="da5d5-131">Resource Group Name</span></span>

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

### <span data-ttu-id="da5d5-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="da5d5-132">-NetworkSetting</span></span>
<span data-ttu-id="da5d5-133">Pobiera ustawienia sieciowe określonego pola danych krawędź/Brama pola danych.</span><span class="sxs-lookup"><span data-stu-id="da5d5-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="da5d5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da5d5-134">-ResourceGroupName</span></span>
<span data-ttu-id="da5d5-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="da5d5-135">Resource Group Name</span></span>

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

### <span data-ttu-id="da5d5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da5d5-136">-ResourceId</span></span>
<span data-ttu-id="da5d5-137">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="da5d5-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="da5d5-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="da5d5-138">-UpdateSummary</span></span>
<span data-ttu-id="da5d5-139">Pobiera informacje o dostępności aktualizacji w oparciu o ostatnie skanowanie urządzenia.</span><span class="sxs-lookup"><span data-stu-id="da5d5-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="da5d5-140">Pobiera również informacje o wszystkich trwających zadaniach pobierania lub instalowania na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="da5d5-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="da5d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5d5-141">CommonParameters</span></span>
<span data-ttu-id="da5d5-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da5d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5d5-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da5d5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5d5-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da5d5-144">INPUTS</span></span>

### <span data-ttu-id="da5d5-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="da5d5-145">None</span></span>

## <span data-ttu-id="da5d5-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da5d5-146">OUTPUTS</span></span>

### <span data-ttu-id="da5d5-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="da5d5-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="da5d5-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="da5d5-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="da5d5-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="da5d5-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="da5d5-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="da5d5-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="da5d5-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="da5d5-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="da5d5-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da5d5-152">NOTES</span></span>

## <span data-ttu-id="da5d5-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da5d5-153">RELATED LINKS</span></span>
