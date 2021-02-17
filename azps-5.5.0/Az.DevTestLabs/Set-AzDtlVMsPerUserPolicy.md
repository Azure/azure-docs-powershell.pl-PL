---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196427"
---
# <span data-ttu-id="07160-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="07160-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="07160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07160-102">SYNOPSIS</span></span>
<span data-ttu-id="07160-103">Ustawia zasady maszyn wirtualnych na użytkownika w laboratorium testów deweloperów.</span><span class="sxs-lookup"><span data-stu-id="07160-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="07160-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07160-104">SYNTAX</span></span>

### <span data-ttu-id="07160-105">Włącz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="07160-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07160-106">Wyłącz</span><span class="sxs-lookup"><span data-stu-id="07160-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07160-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="07160-107">DESCRIPTION</span></span>
<span data-ttu-id="07160-108">Polecenie **cmdlet Set-AzDtlVMsPerUserPolicy** ustawia zasady maszyn wirtualnych na użytkownika w laboratorium, które ustawia maksymalną dozwoloną liczbę maszyn wirtualnych na użytkownika.</span><span class="sxs-lookup"><span data-stu-id="07160-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="07160-109">Polecenie cmdlet używa określonej grupy zasobów i nazwy laboratorium do ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="07160-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="07160-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07160-110">EXAMPLES</span></span>

## <span data-ttu-id="07160-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07160-111">PARAMETERS</span></span>

### <span data-ttu-id="07160-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07160-112">-DefaultProfile</span></span>
<span data-ttu-id="07160-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="07160-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07160-114">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="07160-114">-Disable</span></span>
<span data-ttu-id="07160-115">Wskazuje, że to polecenie cmdlet wyłącza zasady dla laboratorium.</span><span class="sxs-lookup"><span data-stu-id="07160-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="07160-116">— Włącz</span><span class="sxs-lookup"><span data-stu-id="07160-116">-Enable</span></span>
<span data-ttu-id="07160-117">Wskazuje, że to polecenie cmdlet włącza zasady dla laboratorium.</span><span class="sxs-lookup"><span data-stu-id="07160-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="07160-118">— LabName</span><span class="sxs-lookup"><span data-stu-id="07160-118">-LabName</span></span>
<span data-ttu-id="07160-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia maszyny wirtualne na zasady użytkownika.</span><span class="sxs-lookup"><span data-stu-id="07160-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="07160-120">— MaxVMs</span><span class="sxs-lookup"><span data-stu-id="07160-120">-MaxVMs</span></span>
<span data-ttu-id="07160-121">Określa maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="07160-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="07160-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07160-122">-ResourceGroupName</span></span>
<span data-ttu-id="07160-123">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="07160-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="07160-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07160-124">-Confirm</span></span>
<span data-ttu-id="07160-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="07160-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07160-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07160-126">-WhatIf</span></span>
<span data-ttu-id="07160-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07160-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07160-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="07160-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07160-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07160-129">CommonParameters</span></span>
<span data-ttu-id="07160-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07160-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07160-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07160-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07160-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07160-132">INPUTS</span></span>

### <span data-ttu-id="07160-133">System.String</span><span class="sxs-lookup"><span data-stu-id="07160-133">System.String</span></span>

## <span data-ttu-id="07160-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07160-134">OUTPUTS</span></span>

### <span data-ttu-id="07160-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="07160-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="07160-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07160-136">NOTES</span></span>

## <span data-ttu-id="07160-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07160-137">RELATED LINKS</span></span>

[<span data-ttu-id="07160-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="07160-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


