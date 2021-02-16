---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194898"
---
# <span data-ttu-id="351c9-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="351c9-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="351c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="351c9-102">SYNOPSIS</span></span>
<span data-ttu-id="351c9-103">Wywołuje określone akcje na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="351c9-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="351c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="351c9-104">SYNTAX</span></span>

### <span data-ttu-id="351c9-105">InvokeMeterForUpdateParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="351c9-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351c9-106">Invoke NanochUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="351c9-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351c9-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="351c9-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351c9-108">InvokeMeterForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="351c9-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351c9-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="351c9-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351c9-110">Invoke NanochUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="351c9-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351c9-111">Invoke NanochUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="351c9-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351c9-112">InvokeMeterForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="351c9-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351c9-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="351c9-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="351c9-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="351c9-114">DESCRIPTION</span></span>
<span data-ttu-id="351c9-115">Polecenie cmdlet **Invoke-AzDataBoxEdgeDevice** wywoła akcje skanowania, pobierania i instalowania aktualizacji na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="351c9-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="351c9-116">Automatyczne skanowanie jest uruchamiane na urządzeniu codziennie. Możesz jawnie wyzwolić skanowanie, uruchamiając to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="351c9-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="351c9-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="351c9-117">EXAMPLES</span></span>

### <span data-ttu-id="351c9-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="351c9-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="351c9-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="351c9-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="351c9-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="351c9-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="351c9-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="351c9-121">PARAMETERS</span></span>

### <span data-ttu-id="351c9-122">— AsJob</span><span class="sxs-lookup"><span data-stu-id="351c9-122">-AsJob</span></span>
<span data-ttu-id="351c9-123">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="351c9-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="351c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351c9-124">-DefaultProfile</span></span>
<span data-ttu-id="351c9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="351c9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="351c9-126">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="351c9-126">-DeviceObject</span></span>
<span data-ttu-id="351c9-127">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="351c9-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="351c9-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="351c9-128">-FetchUpdate</span></span>
<span data-ttu-id="351c9-129">Pobieranie aktualizacji na urządzeniu z krawędzią/bramą pola danych</span><span class="sxs-lookup"><span data-stu-id="351c9-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="351c9-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="351c9-130">-InstallUpdate</span></span>
<span data-ttu-id="351c9-131">Instaluje aktualizacje na urządzeniu z krawędzią/bramą pola danych</span><span class="sxs-lookup"><span data-stu-id="351c9-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="351c9-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="351c9-132">-Name</span></span>
<span data-ttu-id="351c9-133">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="351c9-133">Device Name</span></span>

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

### <span data-ttu-id="351c9-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="351c9-134">-PassThru</span></span>
<span data-ttu-id="351c9-135">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="351c9-135">returns true if successful</span></span>

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

### <span data-ttu-id="351c9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351c9-136">-ResourceGroupName</span></span>
<span data-ttu-id="351c9-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="351c9-137">Resource Group Name</span></span>

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

### <span data-ttu-id="351c9-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="351c9-138">-ResourceId</span></span>
<span data-ttu-id="351c9-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="351c9-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="351c9-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="351c9-140">-ScanForUpdate</span></span>
<span data-ttu-id="351c9-141">Skanuje w poszukiwaniu aktualizacji na urządzeniu z krawędzią/bramą pola danych.</span><span class="sxs-lookup"><span data-stu-id="351c9-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="351c9-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="351c9-142">-Confirm</span></span>
<span data-ttu-id="351c9-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="351c9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="351c9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="351c9-144">-WhatIf</span></span>
<span data-ttu-id="351c9-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="351c9-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="351c9-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="351c9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="351c9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351c9-147">CommonParameters</span></span>
<span data-ttu-id="351c9-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="351c9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351c9-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="351c9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351c9-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="351c9-150">INPUTS</span></span>

### <span data-ttu-id="351c9-151">Brak</span><span class="sxs-lookup"><span data-stu-id="351c9-151">None</span></span>

## <span data-ttu-id="351c9-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="351c9-152">OUTPUTS</span></span>

### <span data-ttu-id="351c9-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="351c9-153">System.Boolean</span></span>

## <span data-ttu-id="351c9-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="351c9-154">NOTES</span></span>

## <span data-ttu-id="351c9-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="351c9-155">RELATED LINKS</span></span>
