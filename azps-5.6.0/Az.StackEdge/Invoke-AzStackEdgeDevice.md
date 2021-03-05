---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: 63d364ac12d47f5bb15e877e5076550a0cbd3f16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005274"
---
# <span data-ttu-id="4befd-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4befd-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="4befd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4befd-102">SYNOPSIS</span></span>
<span data-ttu-id="4befd-103">Wywołuje określone akcje na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="4befd-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="4befd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4befd-104">SYNTAX</span></span>

### <span data-ttu-id="4befd-105">InvokeBlockForUpdateParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4befd-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4befd-106">Invoke NanochUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4befd-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4befd-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4befd-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4befd-108">InvokeMeterForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4befd-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4befd-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="4befd-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4befd-110">Invoke NanochUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="4befd-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4befd-111">Invoke JednakchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4befd-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4befd-112">InvokeMeterForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4befd-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4befd-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4befd-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4befd-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="4befd-114">DESCRIPTION</span></span>
<span data-ttu-id="4befd-115">Polecenie cmdlet **Invoke-AzStackEdgeDevice** wywoła akcje skanowania, pobierania i instalowania aktualizacji na urządzeniu Ze stosem Edge.</span><span class="sxs-lookup"><span data-stu-id="4befd-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="4befd-116">Automatyczne skanowanie jest uruchamiane na urządzeniu codziennie. Możesz jawnie wyzwolić skanowanie, uruchamiając to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4befd-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="4befd-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4befd-117">EXAMPLES</span></span>

### <span data-ttu-id="4befd-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4befd-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="4befd-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4befd-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="4befd-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4befd-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="4befd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4befd-121">PARAMETERS</span></span>

### <span data-ttu-id="4befd-122">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4befd-122">-AsJob</span></span>
<span data-ttu-id="4befd-123">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4befd-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4befd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4befd-124">-DefaultProfile</span></span>
<span data-ttu-id="4befd-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4befd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4befd-126">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="4befd-126">-DeviceObject</span></span>
<span data-ttu-id="4befd-127">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="4befd-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4befd-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="4befd-128">-FetchUpdate</span></span>
<span data-ttu-id="4befd-129">Pobieranie aktualizacji na urządzeniu z krawędzią/bramą stosową</span><span class="sxs-lookup"><span data-stu-id="4befd-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="4befd-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="4befd-130">-InstallUpdate</span></span>
<span data-ttu-id="4befd-131">Instaluje aktualizacje na urządzeniu z krawędzią/bramą stosową</span><span class="sxs-lookup"><span data-stu-id="4befd-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="4befd-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4befd-132">-Name</span></span>
<span data-ttu-id="4befd-133">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="4befd-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4befd-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4befd-134">-PassThru</span></span>
<span data-ttu-id="4befd-135">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="4befd-135">returns true if successful</span></span>

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

### <span data-ttu-id="4befd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4befd-136">-ResourceGroupName</span></span>
<span data-ttu-id="4befd-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4befd-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4befd-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4befd-138">-ResourceId</span></span>
<span data-ttu-id="4befd-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4befd-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4befd-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="4befd-140">-ScanForUpdate</span></span>
<span data-ttu-id="4befd-141">Skanuje w poszukiwaniu aktualizacji na urządzeniu z bramą/krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="4befd-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="4befd-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4befd-142">-Confirm</span></span>
<span data-ttu-id="4befd-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4befd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4befd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4befd-144">-WhatIf</span></span>
<span data-ttu-id="4befd-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4befd-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4befd-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4befd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4befd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4befd-147">CommonParameters</span></span>
<span data-ttu-id="4befd-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4befd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4befd-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4befd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4befd-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4befd-150">INPUTS</span></span>

### <span data-ttu-id="4befd-151">Brak</span><span class="sxs-lookup"><span data-stu-id="4befd-151">None</span></span>

## <span data-ttu-id="4befd-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4befd-152">OUTPUTS</span></span>

### <span data-ttu-id="4befd-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4befd-153">System.Boolean</span></span>

## <span data-ttu-id="4befd-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4befd-154">NOTES</span></span>

## <span data-ttu-id="4befd-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4befd-155">RELATED LINKS</span></span>
