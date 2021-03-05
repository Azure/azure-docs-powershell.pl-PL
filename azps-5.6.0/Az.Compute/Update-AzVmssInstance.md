---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: ed0ad08d94cbc67832b6a0dbb85882bd18692d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992846"
---
# <span data-ttu-id="d8996-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="d8996-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="d8996-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8996-102">SYNOPSIS</span></span>
<span data-ttu-id="d8996-103">Uruchamia ręczne uaktualnianie wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8996-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="d8996-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8996-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8996-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8996-105">DESCRIPTION</span></span>
<span data-ttu-id="d8996-106">Polecenie Update-AzVmssInstance uruchamia ręczne uaktualnianie określonego wystąpienia zestawu skal maszyn wirtualnych (VIRTUAL MACHINE Scale Set).</span><span class="sxs-lookup"><span data-stu-id="d8996-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="d8996-107">Jest to używane, gdy zasady uaktualniania w zestawie skal maszyny wirtualnej mają ustawioną wartość ręczna.</span><span class="sxs-lookup"><span data-stu-id="d8996-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="d8996-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8996-108">EXAMPLES</span></span>

### <span data-ttu-id="d8996-109">Przykład 1. Rozpoczęcie uaktualniania wystąpienia maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="d8996-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="d8996-110">To polecenie uruchamia uaktualnienie maszyny wirtualnej o nazwie VMScaleSet001 o identyfikatorze wystąpienia 0.</span><span class="sxs-lookup"><span data-stu-id="d8996-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="d8996-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8996-111">PARAMETERS</span></span>

### <span data-ttu-id="d8996-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d8996-112">-AsJob</span></span>
<span data-ttu-id="d8996-113">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="d8996-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d8996-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8996-114">-DefaultProfile</span></span>
<span data-ttu-id="d8996-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8996-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8996-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d8996-116">-InstanceId</span></span>
<span data-ttu-id="d8996-117">Określa jako tablicę ciągów identyfikator lub identyfikatory wystąpienia do uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d8996-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8996-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8996-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8996-119">Określa nazwę grupy zasobów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="d8996-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d8996-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d8996-120">-VMScaleSetName</span></span>
<span data-ttu-id="d8996-121">Określa nazwę wystąpienia maszyny wirtualnej, które uaktualnia to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8996-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="d8996-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8996-122">-Confirm</span></span>
<span data-ttu-id="d8996-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8996-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8996-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8996-124">-WhatIf</span></span>
<span data-ttu-id="d8996-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8996-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8996-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8996-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8996-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8996-127">CommonParameters</span></span>
<span data-ttu-id="d8996-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8996-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8996-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8996-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8996-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8996-130">INPUTS</span></span>

### <span data-ttu-id="d8996-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d8996-131">System.String</span></span>

### <span data-ttu-id="d8996-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d8996-132">System.String[]</span></span>

## <span data-ttu-id="d8996-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8996-133">OUTPUTS</span></span>

### <span data-ttu-id="d8996-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d8996-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d8996-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8996-135">NOTES</span></span>

## <span data-ttu-id="d8996-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8996-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8996-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d8996-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


