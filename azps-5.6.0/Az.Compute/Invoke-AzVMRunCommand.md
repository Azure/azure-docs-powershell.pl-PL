---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 8eaf939839a668ea817d8f3529fced76ef71d22e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004577"
---
# <span data-ttu-id="bfbc2-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="bfbc2-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="bfbc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfbc2-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbc2-103">Uruchamianie polecenia na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-103">Run a command on the VM.</span></span>

## <span data-ttu-id="bfbc2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bfbc2-104">SYNTAX</span></span>

### <span data-ttu-id="bfbc2-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bfbc2-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbc2-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="bfbc2-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfbc2-107">VMParameters</span><span class="sxs-lookup"><span data-stu-id="bfbc2-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfbc2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bfbc2-108">DESCRIPTION</span></span>
<span data-ttu-id="bfbc2-109">Wywołaj polecenie uruchomienia na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="bfbc2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bfbc2-110">EXAMPLES</span></span>

### <span data-ttu-id="bfbc2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bfbc2-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="bfbc2-112">Wywoływanie polecenia uruchom skrypt RunPowerShellScript z zastąpieniem skryptu "sample.ps1" i parametrów maszyny wirtualnej "nazwa_maszyny wirtualnej" w grupie zasobów "nazwa_maszyny wirtualnej".</span><span class="sxs-lookup"><span data-stu-id="bfbc2-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="bfbc2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfbc2-113">PARAMETERS</span></span>

### <span data-ttu-id="bfbc2-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bfbc2-114">-AsJob</span></span>
<span data-ttu-id="bfbc2-115">Uruchom polecenie cmdlet w tle i zwróć obiekt zadania do śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="bfbc2-116">- CommandId</span><span class="sxs-lookup"><span data-stu-id="bfbc2-116">-CommandId</span></span>
<span data-ttu-id="bfbc2-117">Identyfikator polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-117">The run command ID.</span></span>

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

### <span data-ttu-id="bfbc2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbc2-118">-DefaultProfile</span></span>
<span data-ttu-id="bfbc2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfbc2-120">- Parametr</span><span class="sxs-lookup"><span data-stu-id="bfbc2-120">-Parameter</span></span>
<span data-ttu-id="bfbc2-121">Parametry polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-121">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfbc2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfbc2-122">-ResourceGroupName</span></span>
<span data-ttu-id="bfbc2-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbc2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfbc2-124">-ResourceId</span></span>
<span data-ttu-id="bfbc2-125">Identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-125">The resource ID for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbc2-126">- ScriptPath</span><span class="sxs-lookup"><span data-stu-id="bfbc2-126">-ScriptPath</span></span>
<span data-ttu-id="bfbc2-127">Ścieżka skryptu do wykonania.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-127">Path of the script to be executed.</span></span>  <span data-ttu-id="bfbc2-128">Po wpisania tej wartości dany skrypt zastąpi domyślny skrypt polecenia.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-128">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfbc2-129">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="bfbc2-129">-VM</span></span>
<span data-ttu-id="bfbc2-130">Obiekt maszyny wirtualnej PS.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbc2-131">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="bfbc2-131">-VMName</span></span>
<span data-ttu-id="bfbc2-132">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfbc2-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bfbc2-133">-Confirm</span></span>
<span data-ttu-id="bfbc2-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfbc2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfbc2-135">-WhatIf</span></span>
<span data-ttu-id="bfbc2-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfbc2-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfbc2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbc2-138">CommonParameters</span></span>
<span data-ttu-id="bfbc2-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfbc2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbc2-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfbc2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbc2-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfbc2-141">INPUTS</span></span>

### <span data-ttu-id="bfbc2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bfbc2-142">System.String</span></span>

### <span data-ttu-id="bfbc2-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bfbc2-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bfbc2-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfbc2-144">OUTPUTS</span></span>

### <span data-ttu-id="bfbc2-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="bfbc2-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="bfbc2-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bfbc2-146">NOTES</span></span>

## <span data-ttu-id="bfbc2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfbc2-147">RELATED LINKS</span></span>
