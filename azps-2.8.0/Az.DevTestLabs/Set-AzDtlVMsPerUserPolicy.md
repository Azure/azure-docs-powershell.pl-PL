---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 33f60d8246f7235e4be816ad55b69c2ebafe9b0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705566"
---
# <span data-ttu-id="f0cc8-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="f0cc8-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="f0cc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="f0cc8-103">Ustawia zasady dotyczące maszyn wirtualnych według użytkowników laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="f0cc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0cc8-104">SYNTAX</span></span>

### <span data-ttu-id="f0cc8-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f0cc8-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0cc8-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="f0cc8-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0cc8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f0cc8-107">DESCRIPTION</span></span>
<span data-ttu-id="f0cc8-108">Polecenie cmdlet **Set-AzDtlVMsPerUserPolicy** ustawia zasady dotyczące maszyn wirtualnych według użytkowników laboratorium, które ustawia maksymalną liczbę maszyn wirtualnych dozwolonych dla jednego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="f0cc8-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="f0cc8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0cc8-110">EXAMPLES</span></span>

## <span data-ttu-id="f0cc8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0cc8-111">PARAMETERS</span></span>

### <span data-ttu-id="f0cc8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0cc8-112">-DefaultProfile</span></span>
<span data-ttu-id="f0cc8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f0cc8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0cc8-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="f0cc8-114">-Disable</span></span>
<span data-ttu-id="f0cc8-115">Wskazuje, że to polecenie cmdlet wyłącza zasady dla laboratorium.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="f0cc8-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="f0cc8-116">-Enable</span></span>
<span data-ttu-id="f0cc8-117">Wskazuje, że to polecenie cmdlet włącza zasady dla laboratorium.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="f0cc8-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="f0cc8-118">-LabName</span></span>
<span data-ttu-id="f0cc8-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia zasady maszyny wirtualnej na użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="f0cc8-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="f0cc8-120">-MaxVMs</span></span>
<span data-ttu-id="f0cc8-121">Określa maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="f0cc8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0cc8-122">-ResourceGroupName</span></span>
<span data-ttu-id="f0cc8-123">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="f0cc8-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0cc8-124">-Confirm</span></span>
<span data-ttu-id="f0cc8-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0cc8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0cc8-126">-WhatIf</span></span>
<span data-ttu-id="f0cc8-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0cc8-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0cc8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0cc8-129">CommonParameters</span></span>
<span data-ttu-id="f0cc8-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0cc8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0cc8-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0cc8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0cc8-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0cc8-132">INPUTS</span></span>

### <span data-ttu-id="f0cc8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f0cc8-133">System.String</span></span>

## <span data-ttu-id="f0cc8-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0cc8-134">OUTPUTS</span></span>

### <span data-ttu-id="f0cc8-135">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f0cc8-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="f0cc8-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0cc8-136">NOTES</span></span>

## <span data-ttu-id="f0cc8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0cc8-137">RELATED LINKS</span></span>

[<span data-ttu-id="f0cc8-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="f0cc8-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


