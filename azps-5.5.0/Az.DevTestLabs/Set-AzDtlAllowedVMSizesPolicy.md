---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188515"
---
# <span data-ttu-id="79639-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="79639-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="79639-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79639-102">SYNOPSIS</span></span>
<span data-ttu-id="79639-103">Ustawia zasady dozwolonego rozmiaru maszyn wirtualnych laboratorium w laboratorium testów deweloperów.</span><span class="sxs-lookup"><span data-stu-id="79639-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="79639-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79639-104">SYNTAX</span></span>

### <span data-ttu-id="79639-105">Włącz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="79639-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79639-106">Wyłącz</span><span class="sxs-lookup"><span data-stu-id="79639-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79639-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="79639-107">DESCRIPTION</span></span>
<span data-ttu-id="79639-108">Polecenie **cmdlet Set-AzDtlAllowedVMSizesPolicy** ustawia zasady dozwolonych rozmiarów maszyn wirtualnych, określającą listę dozwolonych rozmiarów maszyn wirtualnych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="79639-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="79639-109">Polecenie cmdlet używa określonej grupy zasobów i nazwy laboratorium do ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="79639-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="79639-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79639-110">EXAMPLES</span></span>

## <span data-ttu-id="79639-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79639-111">PARAMETERS</span></span>

### <span data-ttu-id="79639-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79639-112">-DefaultProfile</span></span>
<span data-ttu-id="79639-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="79639-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79639-114">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="79639-114">-Disable</span></span>
<span data-ttu-id="79639-115">Wskazuje, że to polecenie cmdlet wyłącza zasady.</span><span class="sxs-lookup"><span data-stu-id="79639-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="79639-116">— Włącz</span><span class="sxs-lookup"><span data-stu-id="79639-116">-Enable</span></span>
<span data-ttu-id="79639-117">Wskazuje, że to polecenie cmdlet włącza zasady.</span><span class="sxs-lookup"><span data-stu-id="79639-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="79639-118">— LabName</span><span class="sxs-lookup"><span data-stu-id="79639-118">-LabName</span></span>
<span data-ttu-id="79639-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia zasady rozmiarów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="79639-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="79639-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79639-120">-ResourceGroupName</span></span>
<span data-ttu-id="79639-121">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="79639-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="79639-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="79639-122">-VmSizes</span></span>
<span data-ttu-id="79639-123">Określa jako tablicę ciągów listę dozwolonych rozmiarów maszyn wirtualnych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="79639-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="79639-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79639-124">-Confirm</span></span>
<span data-ttu-id="79639-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79639-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79639-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79639-126">-WhatIf</span></span>
<span data-ttu-id="79639-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79639-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79639-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79639-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79639-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79639-129">CommonParameters</span></span>
<span data-ttu-id="79639-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79639-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79639-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79639-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79639-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79639-132">INPUTS</span></span>

### <span data-ttu-id="79639-133">System.String</span><span class="sxs-lookup"><span data-stu-id="79639-133">System.String</span></span>

## <span data-ttu-id="79639-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79639-134">OUTPUTS</span></span>

### <span data-ttu-id="79639-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="79639-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="79639-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79639-136">NOTES</span></span>

## <span data-ttu-id="79639-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79639-137">RELATED LINKS</span></span>

[<span data-ttu-id="79639-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="79639-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


