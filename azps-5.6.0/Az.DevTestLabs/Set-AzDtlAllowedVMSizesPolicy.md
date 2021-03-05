---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 04538710a078c72c7b91725823601a55c21ef846
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994351"
---
# <span data-ttu-id="a0d43-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="a0d43-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="a0d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0d43-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d43-103">Ustawia zasady dozwolonego rozmiaru maszyn wirtualnych laboratorium w laboratorium testów deweloperów.</span><span class="sxs-lookup"><span data-stu-id="a0d43-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="a0d43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0d43-104">SYNTAX</span></span>

### <span data-ttu-id="a0d43-105">Włącz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a0d43-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0d43-106">Wyłącz</span><span class="sxs-lookup"><span data-stu-id="a0d43-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0d43-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0d43-107">DESCRIPTION</span></span>
<span data-ttu-id="a0d43-108">Polecenie **cmdlet Set-AzDtlAllowedVMSizesPolicy** ustawia zasady dozwolonych rozmiarów maszyn wirtualnych, określając listę dozwolonych rozmiarów maszyn wirtualnych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="a0d43-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="a0d43-109">Polecenie cmdlet używa określonej grupy zasobów i nazwy laboratorium do ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="a0d43-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="a0d43-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0d43-110">EXAMPLES</span></span>

## <span data-ttu-id="a0d43-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0d43-111">PARAMETERS</span></span>

### <span data-ttu-id="a0d43-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d43-112">-DefaultProfile</span></span>
<span data-ttu-id="a0d43-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a0d43-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0d43-114">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="a0d43-114">-Disable</span></span>
<span data-ttu-id="a0d43-115">Wskazuje, że to polecenie cmdlet wyłącza zasady.</span><span class="sxs-lookup"><span data-stu-id="a0d43-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d43-116">— Włącz</span><span class="sxs-lookup"><span data-stu-id="a0d43-116">-Enable</span></span>
<span data-ttu-id="a0d43-117">Wskazuje, że to polecenie cmdlet włącza zasady.</span><span class="sxs-lookup"><span data-stu-id="a0d43-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d43-118">— LabName</span><span class="sxs-lookup"><span data-stu-id="a0d43-118">-LabName</span></span>
<span data-ttu-id="a0d43-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet określa zasady rozmiarów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="a0d43-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="a0d43-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d43-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0d43-121">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="a0d43-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d43-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="a0d43-122">-VmSizes</span></span>
<span data-ttu-id="a0d43-123">Określa jako tablicę ciągów listę dozwolonych rozmiarów maszyn wirtualnych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="a0d43-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d43-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0d43-124">-Confirm</span></span>
<span data-ttu-id="a0d43-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a0d43-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d43-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d43-126">-WhatIf</span></span>
<span data-ttu-id="a0d43-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d43-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d43-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a0d43-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d43-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d43-129">CommonParameters</span></span>
<span data-ttu-id="a0d43-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d43-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d43-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d43-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d43-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0d43-132">INPUTS</span></span>

### <span data-ttu-id="a0d43-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a0d43-133">System.String</span></span>

## <span data-ttu-id="a0d43-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0d43-134">OUTPUTS</span></span>

### <span data-ttu-id="a0d43-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a0d43-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a0d43-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0d43-136">NOTES</span></span>

## <span data-ttu-id="a0d43-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0d43-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0d43-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="a0d43-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


