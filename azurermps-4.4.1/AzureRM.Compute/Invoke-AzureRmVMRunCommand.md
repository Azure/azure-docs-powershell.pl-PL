---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 2402591c6c388dbe7c1c6b24a1beb2b298012d4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554210"
---
# <span data-ttu-id="55279-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="55279-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="55279-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55279-102">SYNOPSIS</span></span>
<span data-ttu-id="55279-103">Polecenie Uruchom na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55279-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55279-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55279-104">SYNTAX</span></span>

### <span data-ttu-id="55279-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="55279-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55279-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="55279-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55279-107">Opis</span><span class="sxs-lookup"><span data-stu-id="55279-107">DESCRIPTION</span></span>
<span data-ttu-id="55279-108">Wywoływanie polecenia Uruchom na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55279-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="55279-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55279-109">EXAMPLES</span></span>

### <span data-ttu-id="55279-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55279-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="55279-111">Wywołać polecenie Uruchom dla RunPowerShellScript, zastępując skrypt "sample.ps1" i parametry w maszynie wirtualnej "VMName" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="55279-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="55279-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55279-112">PARAMETERS</span></span>

### <span data-ttu-id="55279-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="55279-113">-CommandId</span></span>
<span data-ttu-id="55279-114">Identyfikator polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="55279-114">The run command id.</span></span>

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

### <span data-ttu-id="55279-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55279-115">-DefaultProfile</span></span>
<span data-ttu-id="55279-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55279-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55279-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="55279-117">-Parameter</span></span>
<span data-ttu-id="55279-118">Parametry polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="55279-118">The run command parameters.</span></span>

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

### <span data-ttu-id="55279-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55279-119">-ResourceGroupName</span></span>
<span data-ttu-id="55279-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55279-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="55279-121">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="55279-121">-ScriptPath</span></span>
<span data-ttu-id="55279-122">Ścieżka skryptu, który ma zostać wykonany.</span><span class="sxs-lookup"><span data-stu-id="55279-122">Path of the script to be executed.</span></span>  <span data-ttu-id="55279-123">Gdy ta wartość zostanie podana, dany skrypt zastąpi domyślny skrypt polecenia.</span><span class="sxs-lookup"><span data-stu-id="55279-123">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="55279-124">-VM</span><span class="sxs-lookup"><span data-stu-id="55279-124">-VM</span></span>
<span data-ttu-id="55279-125">Obiekt maszyny wirtualnej PS.</span><span class="sxs-lookup"><span data-stu-id="55279-125">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="55279-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="55279-126">-VMName</span></span>
<span data-ttu-id="55279-127">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55279-127">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="55279-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55279-128">-Confirm</span></span>
<span data-ttu-id="55279-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55279-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55279-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55279-130">-WhatIf</span></span>
<span data-ttu-id="55279-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55279-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55279-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55279-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55279-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55279-133">CommonParameters</span></span>
<span data-ttu-id="55279-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55279-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55279-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55279-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55279-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55279-136">INPUTS</span></span>

### <span data-ttu-id="55279-137">System. String</span><span class="sxs-lookup"><span data-stu-id="55279-137">System.String</span></span>
<span data-ttu-id="55279-138">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="55279-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="55279-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55279-139">OUTPUTS</span></span>

### <span data-ttu-id="55279-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="55279-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="55279-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55279-141">NOTES</span></span>

## <span data-ttu-id="55279-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55279-142">RELATED LINKS</span></span>

