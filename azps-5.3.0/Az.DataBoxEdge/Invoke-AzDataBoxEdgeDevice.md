---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501639"
---
# <span data-ttu-id="b9e7f-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b9e7f-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b9e7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e7f-103">Wywołuje określone akcje na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="b9e7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9e7f-104">SYNTAX</span></span>

### <span data-ttu-id="b9e7f-105">InvokeScanForUpdateParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b9e7f-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e7f-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e7f-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e7f-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e7f-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e7f-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e7f-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e7f-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e7f-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e7f-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e7f-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e7f-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e7f-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e7f-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e7f-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e7f-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e7f-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e7f-114">Opis</span><span class="sxs-lookup"><span data-stu-id="b9e7f-114">DESCRIPTION</span></span>
<span data-ttu-id="b9e7f-115">Polecenie cmdlet **Invoke-AzDataBoxEdgeDevice** wywołuje akcje skanowania, pobierania i instalowania aktualizacji na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="b9e7f-116">Automatyczne skanowanie jest uruchamiane na urządzeniu codziennie, więc uruchomienie tego polecenia cmdlet może spowodować jawne wykonanie skanowania.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="b9e7f-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9e7f-117">EXAMPLES</span></span>

### <span data-ttu-id="b9e7f-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9e7f-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="b9e7f-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b9e7f-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="b9e7f-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b9e7f-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="b9e7f-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9e7f-121">PARAMETERS</span></span>

### <span data-ttu-id="b9e7f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9e7f-122">-AsJob</span></span>
<span data-ttu-id="b9e7f-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b9e7f-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9e7f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e7f-124">-DefaultProfile</span></span>
<span data-ttu-id="b9e7f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e7f-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b9e7f-126">-DeviceObject</span></span>
<span data-ttu-id="b9e7f-127">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="b9e7f-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7f-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="b9e7f-128">-FetchUpdate</span></span>
<span data-ttu-id="b9e7f-129">Pobiera aktualizacje na urządzeniu z krawędzią/bramą pola danych.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-129">Downloads the updates on a data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7f-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="b9e7f-130">-InstallUpdate</span></span>
<span data-ttu-id="b9e7f-131">Instaluje aktualizacje na urządzeniu z krawędzią/bramą pola danych.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-131">Installs the updates on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7f-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9e7f-132">-Name</span></span>
<span data-ttu-id="b9e7f-133">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="b9e7f-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7f-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9e7f-134">-PassThru</span></span>
<span data-ttu-id="b9e7f-135">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="b9e7f-135">returns true if successful</span></span>

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

### <span data-ttu-id="b9e7f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e7f-136">-ResourceGroupName</span></span>
<span data-ttu-id="b9e7f-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b9e7f-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9e7f-138">-ResourceId</span></span>
<span data-ttu-id="b9e7f-139">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b9e7f-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7f-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="b9e7f-140">-ScanForUpdate</span></span>
<span data-ttu-id="b9e7f-141">Skanuje w poszukiwaniu aktualizacji na urządzeniu z krawędzią/bramą pola danych.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-141">Scans for updates on a data box edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7f-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9e7f-142">-Confirm</span></span>
<span data-ttu-id="b9e7f-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e7f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e7f-144">-WhatIf</span></span>
<span data-ttu-id="b9e7f-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9e7f-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e7f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e7f-147">CommonParameters</span></span>
<span data-ttu-id="b9e7f-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e7f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e7f-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9e7f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e7f-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9e7f-150">INPUTS</span></span>

### <span data-ttu-id="b9e7f-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b9e7f-151">None</span></span>

## <span data-ttu-id="b9e7f-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9e7f-152">OUTPUTS</span></span>

### <span data-ttu-id="b9e7f-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9e7f-153">System.Boolean</span></span>

## <span data-ttu-id="b9e7f-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9e7f-154">NOTES</span></span>

## <span data-ttu-id="b9e7f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9e7f-155">RELATED LINKS</span></span>
