---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 89d81387f8a97fe02f607ddc9d13d4645fc9688b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545488"
---
# <span data-ttu-id="515f9-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="515f9-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="515f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="515f9-102">SYNOPSIS</span></span>
<span data-ttu-id="515f9-103">Polecenie Uruchom na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="515f9-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="515f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="515f9-104">SYNTAX</span></span>

### <span data-ttu-id="515f9-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="515f9-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515f9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="515f9-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="515f9-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="515f9-107">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="515f9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="515f9-108">DESCRIPTION</span></span>
<span data-ttu-id="515f9-109">Wywoływanie polecenia Uruchom na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="515f9-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="515f9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="515f9-110">EXAMPLES</span></span>

### <span data-ttu-id="515f9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="515f9-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="515f9-112">Wywołać polecenie Uruchom dla RunPowerShellScript, zastępując skrypt "sample.ps1" i parametry w maszynie wirtualnej "VMName" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="515f9-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="515f9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="515f9-113">PARAMETERS</span></span>

### <span data-ttu-id="515f9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="515f9-114">-AsJob</span></span>
<span data-ttu-id="515f9-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="515f9-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="515f9-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="515f9-116">-CommandId</span></span>
<span data-ttu-id="515f9-117">Identyfikator polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="515f9-117">The run command id.</span></span>

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

### <span data-ttu-id="515f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515f9-118">-DefaultProfile</span></span>
<span data-ttu-id="515f9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="515f9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515f9-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="515f9-120">-Parameter</span></span>
<span data-ttu-id="515f9-121">Parametry polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="515f9-121">The run command parameters.</span></span>

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

### <span data-ttu-id="515f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="515f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="515f9-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="515f9-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="515f9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="515f9-124">-ResourceId</span></span>
<span data-ttu-id="515f9-125">Identyfikator zasobu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="515f9-125">The resource id for the VM</span></span>

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

### <span data-ttu-id="515f9-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="515f9-126">-ScriptPath</span></span>
<span data-ttu-id="515f9-127">Ścieżka skryptu, który ma zostać wykonany.</span><span class="sxs-lookup"><span data-stu-id="515f9-127">Path of the script to be executed.</span></span>  <span data-ttu-id="515f9-128">Gdy ta wartość zostanie podana, dany skrypt zastąpi domyślny skrypt polecenia.</span><span class="sxs-lookup"><span data-stu-id="515f9-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="515f9-129">-VM</span><span class="sxs-lookup"><span data-stu-id="515f9-129">-VM</span></span>
<span data-ttu-id="515f9-130">Obiekt maszyny wirtualnej PS.</span><span class="sxs-lookup"><span data-stu-id="515f9-130">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="515f9-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="515f9-131">-VMName</span></span>
<span data-ttu-id="515f9-132">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="515f9-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="515f9-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="515f9-133">-Confirm</span></span>
<span data-ttu-id="515f9-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="515f9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="515f9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="515f9-135">-WhatIf</span></span>
<span data-ttu-id="515f9-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="515f9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="515f9-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="515f9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="515f9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515f9-138">CommonParameters</span></span>
<span data-ttu-id="515f9-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="515f9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515f9-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="515f9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515f9-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="515f9-141">INPUTS</span></span>

### <span data-ttu-id="515f9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="515f9-142">System.String</span></span>

### <span data-ttu-id="515f9-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="515f9-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="515f9-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="515f9-144">OUTPUTS</span></span>

### <span data-ttu-id="515f9-145">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="515f9-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="515f9-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="515f9-146">NOTES</span></span>

## <span data-ttu-id="515f9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="515f9-147">RELATED LINKS</span></span>
