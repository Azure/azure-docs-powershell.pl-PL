---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 629ed4d9bc8eeb01f41bb857868f4206afcc9b0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010529"
---
# <span data-ttu-id="fb9aa-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="fb9aa-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="fb9aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9aa-103">Ustawia zasady maszyn wirtualnych na użytkownika w laboratorium testów deweloperów.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="fb9aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb9aa-104">SYNTAX</span></span>

### <span data-ttu-id="fb9aa-105">Włącz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fb9aa-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9aa-106">Wyłącz</span><span class="sxs-lookup"><span data-stu-id="fb9aa-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb9aa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb9aa-107">DESCRIPTION</span></span>
<span data-ttu-id="fb9aa-108">Polecenie **cmdlet Set-AzDtlVMsPerUserPolicy** ustawia zasady maszyn wirtualnych na użytkownika w laboratorium, które ustawia maksymalną dozwoloną liczbę maszyn wirtualnych dla każdego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="fb9aa-109">Polecenie cmdlet używa określonej grupy zasobów i nazwy laboratorium do ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="fb9aa-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb9aa-110">EXAMPLES</span></span>

## <span data-ttu-id="fb9aa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb9aa-111">PARAMETERS</span></span>

### <span data-ttu-id="fb9aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9aa-112">-DefaultProfile</span></span>
<span data-ttu-id="fb9aa-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fb9aa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb9aa-114">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="fb9aa-114">-Disable</span></span>
<span data-ttu-id="fb9aa-115">Wskazuje, że to polecenie cmdlet wyłącza zasady dla laboratorium.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="fb9aa-116">— Włącz</span><span class="sxs-lookup"><span data-stu-id="fb9aa-116">-Enable</span></span>
<span data-ttu-id="fb9aa-117">Wskazuje, że to polecenie cmdlet włącza zasady dla laboratorium.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="fb9aa-118">— LabName</span><span class="sxs-lookup"><span data-stu-id="fb9aa-118">-LabName</span></span>
<span data-ttu-id="fb9aa-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia maszyny wirtualne na zasady użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="fb9aa-120">- MaxVMs</span><span class="sxs-lookup"><span data-stu-id="fb9aa-120">-MaxVMs</span></span>
<span data-ttu-id="fb9aa-121">Określa maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb9aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb9aa-123">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="fb9aa-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb9aa-124">-Confirm</span></span>
<span data-ttu-id="fb9aa-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb9aa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb9aa-126">-WhatIf</span></span>
<span data-ttu-id="fb9aa-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb9aa-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb9aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9aa-129">CommonParameters</span></span>
<span data-ttu-id="fb9aa-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb9aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9aa-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb9aa-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9aa-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb9aa-132">INPUTS</span></span>

### <span data-ttu-id="fb9aa-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fb9aa-133">System.String</span></span>

## <span data-ttu-id="fb9aa-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb9aa-134">OUTPUTS</span></span>

### <span data-ttu-id="fb9aa-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="fb9aa-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="fb9aa-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb9aa-136">NOTES</span></span>

## <span data-ttu-id="fb9aa-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb9aa-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb9aa-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="fb9aa-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


