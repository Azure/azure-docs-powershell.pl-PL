---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: fb3d6f08eaa540e208830a15563b8edd8c2432ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962449"
---
# <span data-ttu-id="aec62-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="aec62-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="aec62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aec62-102">SYNOPSIS</span></span>
<span data-ttu-id="aec62-103">Rozpoczyna uaktualnianie w celu przeniesienia wszystkich wystąpień zestawu skal maszyn wirtualnych do najnowszej dostępnej wersji systemu operacyjnego w wersji Obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="aec62-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="aec62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aec62-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec62-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="aec62-105">DESCRIPTION</span></span>
<span data-ttu-id="aec62-106">Rozpoczyna uaktualnianie w celu przeniesienia wszystkich wystąpień zestawu skal maszyn wirtualnych do najnowszej dostępnej wersji systemu operacyjnego w wersji Obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="aec62-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="aec62-107">Nie wpływa to na wystąpienia, w których jest już uruchomiona najnowsza dostępna wersja systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="aec62-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="aec62-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aec62-108">EXAMPLES</span></span>

### <span data-ttu-id="aec62-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aec62-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="aec62-110">To polecenie uruchamia uaktualnianie stopniowe wszystkich wystąpień maszyny wirtualnej zestawu skali maszyny wirtualnej "MASZYNY WIRTUALNE", które jest "MASZYNY WIRTUALNE0001" w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="aec62-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="aec62-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aec62-111">PARAMETERS</span></span>

### <span data-ttu-id="aec62-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="aec62-112">-AsJob</span></span>
<span data-ttu-id="aec62-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="aec62-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aec62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec62-114">-DefaultProfile</span></span>
<span data-ttu-id="aec62-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aec62-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aec62-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec62-116">-ResourceGroupName</span></span>
<span data-ttu-id="aec62-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aec62-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="aec62-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="aec62-118">-VMScaleSetName</span></span>
<span data-ttu-id="aec62-119">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aec62-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="aec62-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aec62-120">-Confirm</span></span>
<span data-ttu-id="aec62-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aec62-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec62-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec62-122">-WhatIf</span></span>
<span data-ttu-id="aec62-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec62-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec62-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aec62-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec62-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec62-125">CommonParameters</span></span>
<span data-ttu-id="aec62-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec62-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec62-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aec62-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec62-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aec62-128">INPUTS</span></span>

### <span data-ttu-id="aec62-129">System.String</span><span class="sxs-lookup"><span data-stu-id="aec62-129">System.String</span></span>

## <span data-ttu-id="aec62-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aec62-130">OUTPUTS</span></span>

### <span data-ttu-id="aec62-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="aec62-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="aec62-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aec62-132">NOTES</span></span>

## <span data-ttu-id="aec62-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aec62-133">RELATED LINKS</span></span>
