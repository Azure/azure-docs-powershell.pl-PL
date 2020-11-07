---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
ms.openlocfilehash: 12b9b3870b5239746a8524bad9aad0f44161acd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898797"
---
# <span data-ttu-id="900b8-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="900b8-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="900b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="900b8-102">SYNOPSIS</span></span>
<span data-ttu-id="900b8-103">Polecenie Uruchom na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="900b8-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="900b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="900b8-104">SYNTAX</span></span>

### <span data-ttu-id="900b8-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="900b8-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="900b8-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="900b8-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="900b8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="900b8-107">DESCRIPTION</span></span>
<span data-ttu-id="900b8-108">Wywoływanie polecenia Uruchom na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="900b8-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="900b8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="900b8-109">EXAMPLES</span></span>

### <span data-ttu-id="900b8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="900b8-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="900b8-111">Wywołać polecenie Uruchom dla RunPowerShellScript, zastępując skrypt "sample.ps1" i parametry w maszynie wirtualnej "VMName" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="900b8-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="900b8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="900b8-112">PARAMETERS</span></span>

### <span data-ttu-id="900b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="900b8-113">-AsJob</span></span>
<span data-ttu-id="900b8-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="900b8-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="900b8-115">-CommandId</span></span>
<span data-ttu-id="900b8-116">Identyfikator polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="900b8-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="900b8-117">-DefaultProfile</span></span>
<span data-ttu-id="900b8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="900b8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="900b8-119">-Parameter</span></span>
<span data-ttu-id="900b8-120">Parametry polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="900b8-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="900b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="900b8-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="900b8-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="900b8-123">-ScriptPath</span></span>
<span data-ttu-id="900b8-124">Ścieżka skryptu, który ma zostać wykonany.</span><span class="sxs-lookup"><span data-stu-id="900b8-124">Path of the script to be executed.</span></span>  <span data-ttu-id="900b8-125">Gdy ta wartość zostanie podana, dany skrypt zastąpi domyślny skrypt polecenia.</span><span class="sxs-lookup"><span data-stu-id="900b8-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-126">-VM</span><span class="sxs-lookup"><span data-stu-id="900b8-126">-VM</span></span>
<span data-ttu-id="900b8-127">Obiekt maszyny wirtualnej PS.</span><span class="sxs-lookup"><span data-stu-id="900b8-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="900b8-128">-VMName</span></span>
<span data-ttu-id="900b8-129">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="900b8-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="900b8-130">-Confirm</span></span>
<span data-ttu-id="900b8-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="900b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="900b8-132">-WhatIf</span></span>
<span data-ttu-id="900b8-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="900b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="900b8-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="900b8-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="900b8-135">CommonParameters</span></span>
<span data-ttu-id="900b8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="900b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="900b8-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="900b8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="900b8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="900b8-138">INPUTS</span></span>

### <span data-ttu-id="900b8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="900b8-139">System.String</span></span>
<span data-ttu-id="900b8-140">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="900b8-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="900b8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="900b8-141">OUTPUTS</span></span>

### <span data-ttu-id="900b8-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="900b8-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="900b8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="900b8-143">NOTES</span></span>

## <span data-ttu-id="900b8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="900b8-144">RELATED LINKS</span></span>

