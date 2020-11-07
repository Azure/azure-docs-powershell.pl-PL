---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3bfd8aad0c88f6a2cd6dfb27124f92605b8a17b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718332"
---
# <span data-ttu-id="1cbe3-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="1cbe3-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="1cbe3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1cbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbe3-103">Ustawia maszyny wirtualne na zasadę laboratoryjną laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cbe3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1cbe3-104">SYNTAX</span></span>

### <span data-ttu-id="1cbe3-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1cbe3-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cbe3-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="1cbe3-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cbe3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1cbe3-107">DESCRIPTION</span></span>
<span data-ttu-id="1cbe3-108">Polecenie cmdlet **Set-AzureRmDtlVMsPerLabPolicy** ustawia maszyny wirtualne według zasad laboratorium laboratorium, które ustawia całkowitą liczbę maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="1cbe3-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="1cbe3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1cbe3-110">EXAMPLES</span></span>

## <span data-ttu-id="1cbe3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1cbe3-111">PARAMETERS</span></span>

### <span data-ttu-id="1cbe3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbe3-112">-DefaultProfile</span></span>
<span data-ttu-id="1cbe3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1cbe3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbe3-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="1cbe3-114">-Disable</span></span>
<span data-ttu-id="1cbe3-115">Wskazuje, że to polecenie cmdlet wyłącza zasady laboratorium.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="1cbe3-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="1cbe3-116">-Enable</span></span>
<span data-ttu-id="1cbe3-117">Wskazuje, że to polecenie cmdlet włącza zasady laboratorium.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="1cbe3-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="1cbe3-118">-LabName</span></span>
<span data-ttu-id="1cbe3-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia maszyny wirtualne według zasad laboratorium.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="1cbe3-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="1cbe3-120">-MaxVMs</span></span>
<span data-ttu-id="1cbe3-121">Określa maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="1cbe3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cbe3-122">-ResourceGroupName</span></span>
<span data-ttu-id="1cbe3-123">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="1cbe3-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1cbe3-124">-Confirm</span></span>
<span data-ttu-id="1cbe3-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cbe3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cbe3-126">-WhatIf</span></span>
<span data-ttu-id="1cbe3-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cbe3-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cbe3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbe3-129">CommonParameters</span></span>
<span data-ttu-id="1cbe3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cbe3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbe3-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cbe3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbe3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cbe3-132">INPUTS</span></span>

### <span data-ttu-id="1cbe3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1cbe3-133">System.String</span></span>

## <span data-ttu-id="1cbe3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1cbe3-134">OUTPUTS</span></span>

### <span data-ttu-id="1cbe3-135">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1cbe3-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="1cbe3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1cbe3-136">NOTES</span></span>

## <span data-ttu-id="1cbe3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1cbe3-137">RELATED LINKS</span></span>

[<span data-ttu-id="1cbe3-138">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="1cbe3-138">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)

