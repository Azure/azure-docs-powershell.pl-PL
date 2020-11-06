---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: e1c5fad70147300bb08fdafb94fb81079a02ea00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542611"
---
# <span data-ttu-id="98842-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="98842-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="98842-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98842-102">SYNOPSIS</span></span>
<span data-ttu-id="98842-103">Ustawia dozwolone zasady rozmiarów maszyn wirtualnych w laboratorium w laboratoriach DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="98842-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98842-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98842-104">SYNTAX</span></span>

### <span data-ttu-id="98842-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="98842-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98842-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="98842-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98842-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98842-107">DESCRIPTION</span></span>
<span data-ttu-id="98842-108">Polecenie cmdlet **Set-AzureRmDtlAllowedVMSizesPolicy** ustawia dozwolone zasady rozmiarów maszyn wirtualnych, które określają listę rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="98842-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="98842-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="98842-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="98842-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98842-110">EXAMPLES</span></span>

## <span data-ttu-id="98842-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98842-111">PARAMETERS</span></span>

### <span data-ttu-id="98842-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98842-112">-DefaultProfile</span></span>
<span data-ttu-id="98842-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="98842-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98842-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="98842-114">-Disable</span></span>
<span data-ttu-id="98842-115">Wskazuje, że to polecenie cmdlet wyłącza zasady.</span><span class="sxs-lookup"><span data-stu-id="98842-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="98842-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="98842-116">-Enable</span></span>
<span data-ttu-id="98842-117">Wskazuje, że to polecenie cmdlet włącza zasady.</span><span class="sxs-lookup"><span data-stu-id="98842-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="98842-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="98842-118">-LabName</span></span>
<span data-ttu-id="98842-119">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia zasady rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98842-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="98842-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98842-120">-ResourceGroupName</span></span>
<span data-ttu-id="98842-121">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="98842-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="98842-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="98842-122">-VmSizes</span></span>
<span data-ttu-id="98842-123">Określa w postaci tablicy ciągów listę rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="98842-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98842-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98842-124">-Confirm</span></span>
<span data-ttu-id="98842-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98842-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98842-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98842-126">-WhatIf</span></span>
<span data-ttu-id="98842-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98842-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98842-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98842-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98842-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98842-129">CommonParameters</span></span>
<span data-ttu-id="98842-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98842-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98842-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98842-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98842-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98842-132">INPUTS</span></span>

### <span data-ttu-id="98842-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="98842-133">None</span></span>
<span data-ttu-id="98842-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="98842-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98842-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98842-135">OUTPUTS</span></span>

### <span data-ttu-id="98842-136">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="98842-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="98842-137">To polecenie cmdlet zwraca zasady określające listę rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="98842-137">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="98842-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98842-138">NOTES</span></span>

## <span data-ttu-id="98842-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98842-139">RELATED LINKS</span></span>

[<span data-ttu-id="98842-140">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="98842-140">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)


