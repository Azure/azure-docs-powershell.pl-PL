---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374432"
---
# <span data-ttu-id="9a659-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9a659-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="9a659-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a659-102">SYNOPSIS</span></span>
<span data-ttu-id="9a659-103">Wywołuje określone akcje na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="9a659-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="9a659-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a659-104">SYNTAX</span></span>

### <span data-ttu-id="9a659-105">InvokeScanForUpdateParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9a659-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a659-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a659-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a659-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a659-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a659-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a659-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a659-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a659-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a659-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a659-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a659-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a659-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a659-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a659-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a659-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a659-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a659-114">Opis</span><span class="sxs-lookup"><span data-stu-id="9a659-114">DESCRIPTION</span></span>
<span data-ttu-id="9a659-115">Polecenie cmdlet **Invoke-AzStackEdgeDevice** wywołuje akcje skanowania, pobierania i instalowania aktualizacji na urządzeniu ze stosem.</span><span class="sxs-lookup"><span data-stu-id="9a659-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="9a659-116">Automatyczne skanowanie jest uruchamiane na urządzeniu codziennie, więc uruchomienie tego polecenia cmdlet może spowodować jawne wykonanie skanowania.</span><span class="sxs-lookup"><span data-stu-id="9a659-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="9a659-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a659-117">EXAMPLES</span></span>

### <span data-ttu-id="9a659-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a659-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="9a659-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9a659-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="9a659-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9a659-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="9a659-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a659-121">PARAMETERS</span></span>

### <span data-ttu-id="9a659-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a659-122">-AsJob</span></span>
<span data-ttu-id="9a659-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9a659-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a659-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a659-124">-DefaultProfile</span></span>
<span data-ttu-id="9a659-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a659-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a659-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9a659-126">-DeviceObject</span></span>
<span data-ttu-id="9a659-127">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="9a659-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="9a659-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="9a659-128">-FetchUpdate</span></span>
<span data-ttu-id="9a659-129">Pobiera aktualizacje na urządzeniu z krawędzią/bramą stosu</span><span class="sxs-lookup"><span data-stu-id="9a659-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="9a659-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="9a659-130">-InstallUpdate</span></span>
<span data-ttu-id="9a659-131">Instaluje aktualizacje na urządzeniu z krawędzią/bramą stosu</span><span class="sxs-lookup"><span data-stu-id="9a659-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="9a659-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a659-132">-Name</span></span>
<span data-ttu-id="9a659-133">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="9a659-133">Device Name</span></span>

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

### <span data-ttu-id="9a659-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a659-134">-PassThru</span></span>
<span data-ttu-id="9a659-135">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="9a659-135">returns true if successful</span></span>

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

### <span data-ttu-id="9a659-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a659-136">-ResourceGroupName</span></span>
<span data-ttu-id="9a659-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9a659-137">Resource Group Name</span></span>

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

### <span data-ttu-id="9a659-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a659-138">-ResourceId</span></span>
<span data-ttu-id="9a659-139">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9a659-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="9a659-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="9a659-140">-ScanForUpdate</span></span>
<span data-ttu-id="9a659-141">Skanuje aktualizacje na urządzeniu z krawędzią/bramą stosu.</span><span class="sxs-lookup"><span data-stu-id="9a659-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="9a659-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a659-142">-Confirm</span></span>
<span data-ttu-id="9a659-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a659-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a659-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a659-144">-WhatIf</span></span>
<span data-ttu-id="9a659-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a659-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a659-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a659-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a659-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a659-147">CommonParameters</span></span>
<span data-ttu-id="9a659-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a659-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a659-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a659-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a659-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a659-150">INPUTS</span></span>

### <span data-ttu-id="9a659-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9a659-151">None</span></span>

## <span data-ttu-id="9a659-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a659-152">OUTPUTS</span></span>

### <span data-ttu-id="9a659-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a659-153">System.Boolean</span></span>

## <span data-ttu-id="9a659-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a659-154">NOTES</span></span>

## <span data-ttu-id="9a659-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a659-155">RELATED LINKS</span></span>
