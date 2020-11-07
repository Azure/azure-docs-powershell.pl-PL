---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 8e6e50fd22330073d647353232c549579aa382a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717533"
---
# <span data-ttu-id="d49c6-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d49c6-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="d49c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d49c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d49c6-103">Ustawia maszyny wirtualne na zasadę laboratoryjną laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="d49c6-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d49c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d49c6-104">SYNTAX</span></span>

### <span data-ttu-id="d49c6-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d49c6-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d49c6-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="d49c6-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d49c6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d49c6-107">DESCRIPTION</span></span>
<span data-ttu-id="d49c6-108">Polecenie cmdlet **Set-AzureRmDtlVMsPerLabPolicy** ustawia maszyny wirtualne według zasad laboratorium laboratorium, które ustawia całkowitą liczbę maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d49c6-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="d49c6-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="d49c6-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="d49c6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d49c6-110">EXAMPLES</span></span>

## <span data-ttu-id="d49c6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d49c6-111">PARAMETERS</span></span>

### <span data-ttu-id="d49c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49c6-112">-DefaultProfile</span></span>
<span data-ttu-id="d49c6-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d49c6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49c6-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="d49c6-114">-Disable</span></span>
<span data-ttu-id="d49c6-115">Wskazuje, że to polecenie cmdlet wyłącza zasady laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d49c6-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49c6-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="d49c6-116">-Enable</span></span>
<span data-ttu-id="d49c6-117">Wskazuje, że to polecenie cmdlet włącza zasady laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d49c6-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49c6-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="d49c6-118">-LabName</span></span>
<span data-ttu-id="d49c6-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia maszyny wirtualne według zasad laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d49c6-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49c6-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="d49c6-120">-MaxVMs</span></span>
<span data-ttu-id="d49c6-121">Określa maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d49c6-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d49c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="d49c6-123">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d49c6-123">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49c6-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d49c6-124">-Confirm</span></span>
<span data-ttu-id="d49c6-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d49c6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49c6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d49c6-126">-WhatIf</span></span>
<span data-ttu-id="d49c6-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d49c6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d49c6-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d49c6-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49c6-129">CommonParameters</span></span>
<span data-ttu-id="d49c6-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d49c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49c6-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49c6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49c6-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d49c6-132">INPUTS</span></span>

### <span data-ttu-id="d49c6-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d49c6-133">None</span></span>
<span data-ttu-id="d49c6-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d49c6-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d49c6-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d49c6-135">OUTPUTS</span></span>

### <span data-ttu-id="d49c6-136">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d49c6-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="d49c6-137">To polecenie cmdlet zwraca zasadę określającą maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d49c6-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="d49c6-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d49c6-138">NOTES</span></span>

## <span data-ttu-id="d49c6-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d49c6-139">RELATED LINKS</span></span>

[<span data-ttu-id="d49c6-140">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d49c6-140">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)


