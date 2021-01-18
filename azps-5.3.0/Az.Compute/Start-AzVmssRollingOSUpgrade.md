---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503932"
---
# <span data-ttu-id="a7f2c-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a7f2c-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="a7f2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f2c-103">Rozpoczyna uaktualnienie stopniowe, aby przenieść wszystkie wystąpienia zestawu skali maszyny wirtualnej na najnowszą dostępną wersję systemu operacyjnego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="a7f2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7f2c-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7f2c-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f2c-106">Rozpoczyna uaktualnienie stopniowe, aby przenieść wszystkie wystąpienia zestawu skali maszyny wirtualnej na najnowszą dostępną wersję systemu operacyjnego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="a7f2c-107">Wystąpienia, na których jest już uruchomiona najnowsza dostępna wersja systemu operacyjnego, nie mają wpływu.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="a7f2c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7f2c-108">EXAMPLES</span></span>

### <span data-ttu-id="a7f2c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7f2c-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a7f2c-110">To polecenie uruchamia uaktualnianie stopniowe wszystkich wystąpień maszyny wirtualnej "VMSS001" w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="a7f2c-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="a7f2c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7f2c-111">PARAMETERS</span></span>

### <span data-ttu-id="a7f2c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7f2c-112">-AsJob</span></span>
<span data-ttu-id="a7f2c-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a7f2c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7f2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f2c-114">-DefaultProfile</span></span>
<span data-ttu-id="a7f2c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f2c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f2c-116">-ResourceGroupName</span></span>
<span data-ttu-id="a7f2c-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f2c-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a7f2c-118">-VMScaleSetName</span></span>
<span data-ttu-id="a7f2c-119">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-119">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f2c-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7f2c-120">-Confirm</span></span>
<span data-ttu-id="a7f2c-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f2c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f2c-122">-WhatIf</span></span>
<span data-ttu-id="a7f2c-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f2c-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f2c-125">CommonParameters</span></span>
<span data-ttu-id="a7f2c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f2c-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7f2c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f2c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7f2c-128">INPUTS</span></span>

### <span data-ttu-id="a7f2c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a7f2c-129">System.String</span></span>

## <span data-ttu-id="a7f2c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7f2c-130">OUTPUTS</span></span>

### <span data-ttu-id="a7f2c-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a7f2c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a7f2c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7f2c-132">NOTES</span></span>

## <span data-ttu-id="a7f2c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7f2c-133">RELATED LINKS</span></span>
