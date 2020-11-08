---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3e06b4f1236863e208a167024e9d0562dc82ca89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224506"
---
# <span data-ttu-id="29bfc-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="29bfc-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="29bfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="29bfc-103">Ustawia maszyny wirtualne na zasadę laboratoryjną laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="29bfc-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="29bfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29bfc-104">SYNTAX</span></span>

### <span data-ttu-id="29bfc-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="29bfc-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29bfc-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="29bfc-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29bfc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="29bfc-107">DESCRIPTION</span></span>
<span data-ttu-id="29bfc-108">Polecenie cmdlet **Set-AzDtlVMsPerLabPolicy** ustawia maszyny wirtualne według zasad laboratorium laboratorium, które ustawia całkowitą liczbę maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="29bfc-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="29bfc-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="29bfc-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="29bfc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29bfc-110">EXAMPLES</span></span>

## <span data-ttu-id="29bfc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29bfc-111">PARAMETERS</span></span>

### <span data-ttu-id="29bfc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bfc-112">-DefaultProfile</span></span>
<span data-ttu-id="29bfc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="29bfc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29bfc-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="29bfc-114">-Disable</span></span>
<span data-ttu-id="29bfc-115">Wskazuje, że to polecenie cmdlet wyłącza zasady laboratorium.</span><span class="sxs-lookup"><span data-stu-id="29bfc-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="29bfc-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="29bfc-116">-Enable</span></span>
<span data-ttu-id="29bfc-117">Wskazuje, że to polecenie cmdlet włącza zasady laboratorium.</span><span class="sxs-lookup"><span data-stu-id="29bfc-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="29bfc-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="29bfc-118">-LabName</span></span>
<span data-ttu-id="29bfc-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia maszyny wirtualne według zasad laboratorium.</span><span class="sxs-lookup"><span data-stu-id="29bfc-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="29bfc-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="29bfc-120">-MaxVMs</span></span>
<span data-ttu-id="29bfc-121">Określa maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="29bfc-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="29bfc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bfc-122">-ResourceGroupName</span></span>
<span data-ttu-id="29bfc-123">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="29bfc-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="29bfc-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29bfc-124">-Confirm</span></span>
<span data-ttu-id="29bfc-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bfc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bfc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bfc-126">-WhatIf</span></span>
<span data-ttu-id="29bfc-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bfc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29bfc-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29bfc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bfc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bfc-129">CommonParameters</span></span>
<span data-ttu-id="29bfc-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29bfc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bfc-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29bfc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bfc-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29bfc-132">INPUTS</span></span>

### <span data-ttu-id="29bfc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="29bfc-133">System.String</span></span>

## <span data-ttu-id="29bfc-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29bfc-134">OUTPUTS</span></span>

### <span data-ttu-id="29bfc-135">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="29bfc-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="29bfc-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29bfc-136">NOTES</span></span>

## <span data-ttu-id="29bfc-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29bfc-137">RELATED LINKS</span></span>

[<span data-ttu-id="29bfc-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="29bfc-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


