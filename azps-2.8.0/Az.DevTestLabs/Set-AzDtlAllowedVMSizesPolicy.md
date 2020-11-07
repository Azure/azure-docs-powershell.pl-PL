---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 9d41e3c4c91a61a12ac18becb4b996bfbe52dbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705572"
---
# <span data-ttu-id="11b30-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="11b30-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="11b30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11b30-102">SYNOPSIS</span></span>
<span data-ttu-id="11b30-103">Ustawia dozwolone zasady rozmiarów maszyn wirtualnych w laboratorium w laboratoriach DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="11b30-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="11b30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11b30-104">SYNTAX</span></span>

### <span data-ttu-id="11b30-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="11b30-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11b30-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="11b30-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11b30-107">Opis</span><span class="sxs-lookup"><span data-stu-id="11b30-107">DESCRIPTION</span></span>
<span data-ttu-id="11b30-108">Polecenie cmdlet **Set-AzDtlAllowedVMSizesPolicy** ustawia dozwolone zasady rozmiarów maszyn wirtualnych, które określają listę rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="11b30-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="11b30-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="11b30-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="11b30-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11b30-110">EXAMPLES</span></span>

## <span data-ttu-id="11b30-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11b30-111">PARAMETERS</span></span>

### <span data-ttu-id="11b30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b30-112">-DefaultProfile</span></span>
<span data-ttu-id="11b30-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="11b30-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11b30-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="11b30-114">-Disable</span></span>
<span data-ttu-id="11b30-115">Wskazuje, że to polecenie cmdlet wyłącza zasady.</span><span class="sxs-lookup"><span data-stu-id="11b30-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="11b30-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="11b30-116">-Enable</span></span>
<span data-ttu-id="11b30-117">Wskazuje, że to polecenie cmdlet włącza zasady.</span><span class="sxs-lookup"><span data-stu-id="11b30-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="11b30-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="11b30-118">-LabName</span></span>
<span data-ttu-id="11b30-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia zasady rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="11b30-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="11b30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b30-120">-ResourceGroupName</span></span>
<span data-ttu-id="11b30-121">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="11b30-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="11b30-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="11b30-122">-VmSizes</span></span>
<span data-ttu-id="11b30-123">Określa w postaci tablicy ciągów listę rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="11b30-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="11b30-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11b30-124">-Confirm</span></span>
<span data-ttu-id="11b30-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b30-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b30-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b30-126">-WhatIf</span></span>
<span data-ttu-id="11b30-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b30-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b30-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11b30-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b30-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b30-129">CommonParameters</span></span>
<span data-ttu-id="11b30-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b30-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b30-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b30-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b30-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11b30-132">INPUTS</span></span>

### <span data-ttu-id="11b30-133">System. String</span><span class="sxs-lookup"><span data-stu-id="11b30-133">System.String</span></span>

## <span data-ttu-id="11b30-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11b30-134">OUTPUTS</span></span>

### <span data-ttu-id="11b30-135">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="11b30-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="11b30-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11b30-136">NOTES</span></span>

## <span data-ttu-id="11b30-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11b30-137">RELATED LINKS</span></span>

[<span data-ttu-id="11b30-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="11b30-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


