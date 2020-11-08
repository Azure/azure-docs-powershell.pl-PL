---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050448"
---
# <span data-ttu-id="57c04-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="57c04-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="57c04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57c04-102">SYNOPSIS</span></span>
<span data-ttu-id="57c04-103">Uruchom polecenie na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57c04-103">Run a command on the VM.</span></span>

## <span data-ttu-id="57c04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57c04-104">SYNTAX</span></span>

### <span data-ttu-id="57c04-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="57c04-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57c04-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="57c04-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57c04-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="57c04-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57c04-108">Opis</span><span class="sxs-lookup"><span data-stu-id="57c04-108">DESCRIPTION</span></span>
<span data-ttu-id="57c04-109">Wywoływanie polecenia Uruchom na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57c04-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="57c04-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57c04-110">EXAMPLES</span></span>

### <span data-ttu-id="57c04-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57c04-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="57c04-112">Wywołać polecenie Uruchom dla RunPowerShellScript, zastępując skrypt "sample.ps1" i parametry w maszynie wirtualnej "VMName" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="57c04-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="57c04-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57c04-113">PARAMETERS</span></span>

### <span data-ttu-id="57c04-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57c04-114">-AsJob</span></span>
<span data-ttu-id="57c04-115">Uruchom polecenie cmdlet w tle i zwróć obiekt zadania w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="57c04-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="57c04-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="57c04-116">-CommandId</span></span>
<span data-ttu-id="57c04-117">Identyfikator polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="57c04-117">The run command ID.</span></span>

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

### <span data-ttu-id="57c04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c04-118">-DefaultProfile</span></span>
<span data-ttu-id="57c04-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57c04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57c04-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="57c04-120">-Parameter</span></span>
<span data-ttu-id="57c04-121">Parametry polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="57c04-121">The run command parameters.</span></span>

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

### <span data-ttu-id="57c04-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c04-122">-ResourceGroupName</span></span>
<span data-ttu-id="57c04-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57c04-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="57c04-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57c04-124">-ResourceId</span></span>
<span data-ttu-id="57c04-125">Identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57c04-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="57c04-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="57c04-126">-ScriptPath</span></span>
<span data-ttu-id="57c04-127">Ścieżka skryptu, który ma zostać wykonany.</span><span class="sxs-lookup"><span data-stu-id="57c04-127">Path of the script to be executed.</span></span>  <span data-ttu-id="57c04-128">Gdy ta wartość zostanie podana, dany skrypt zastąpi domyślny skrypt polecenia.</span><span class="sxs-lookup"><span data-stu-id="57c04-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="57c04-129">-VM</span><span class="sxs-lookup"><span data-stu-id="57c04-129">-VM</span></span>
<span data-ttu-id="57c04-130">Obiekt maszyny wirtualnej PS.</span><span class="sxs-lookup"><span data-stu-id="57c04-130">The PS virtual machine object.</span></span>

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

### <span data-ttu-id="57c04-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="57c04-131">-VMName</span></span>
<span data-ttu-id="57c04-132">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57c04-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="57c04-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57c04-133">-Confirm</span></span>
<span data-ttu-id="57c04-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c04-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c04-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c04-135">-WhatIf</span></span>
<span data-ttu-id="57c04-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c04-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c04-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57c04-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c04-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c04-138">CommonParameters</span></span>
<span data-ttu-id="57c04-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c04-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c04-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57c04-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c04-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57c04-141">INPUTS</span></span>

### <span data-ttu-id="57c04-142">System. String</span><span class="sxs-lookup"><span data-stu-id="57c04-142">System.String</span></span>

### <span data-ttu-id="57c04-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="57c04-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="57c04-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57c04-144">OUTPUTS</span></span>

### <span data-ttu-id="57c04-145">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="57c04-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="57c04-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57c04-146">NOTES</span></span>

## <span data-ttu-id="57c04-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57c04-147">RELATED LINKS</span></span>
