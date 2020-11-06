---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 8cc571a9ba906ecc5556d920503712ef1bb3587a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546655"
---
# <span data-ttu-id="e85cc-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="e85cc-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="e85cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e85cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e85cc-103">Ustawia zasady automatycznego uruchamiania laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="e85cc-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e85cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e85cc-104">SYNTAX</span></span>

### <span data-ttu-id="e85cc-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e85cc-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e85cc-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="e85cc-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e85cc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e85cc-107">DESCRIPTION</span></span>
<span data-ttu-id="e85cc-108">Polecenie cmdlet **Set-AzureRmDtlAutoStartPolicy** ustawia zasady automatycznego uruchamiania laboratorium, które umożliwia planowanie maszyn wirtualnych laboratorium w celu automatycznego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="e85cc-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="e85cc-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="e85cc-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="e85cc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e85cc-110">EXAMPLES</span></span>

## <span data-ttu-id="e85cc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e85cc-111">PARAMETERS</span></span>

### <span data-ttu-id="e85cc-112">-Dni</span><span class="sxs-lookup"><span data-stu-id="e85cc-112">-Days</span></span>
<span data-ttu-id="e85cc-113">Określa jako tablicę dni tygodnia, w których muszą być uruchamiane maszyny wirtualne laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e85cc-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85cc-114">-DefaultProfile</span></span>
<span data-ttu-id="e85cc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e85cc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e85cc-116">-Disable</span><span class="sxs-lookup"><span data-stu-id="e85cc-116">-Disable</span></span>
<span data-ttu-id="e85cc-117">Wskazuje, że to polecenie cmdlet wyłącza zasady dla maszyn wirtualnych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e85cc-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="e85cc-118">-Enable</span><span class="sxs-lookup"><span data-stu-id="e85cc-118">-Enable</span></span>
<span data-ttu-id="e85cc-119">Wskazuje, że to polecenie cmdlet włącza zasady dla maszyn wirtualnych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e85cc-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="e85cc-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="e85cc-120">-LabName</span></span>
<span data-ttu-id="e85cc-121">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia zasadę uruchamiania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="e85cc-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="e85cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e85cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="e85cc-123">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e85cc-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="e85cc-124">-Time (czas)</span><span class="sxs-lookup"><span data-stu-id="e85cc-124">-Time</span></span>
<span data-ttu-id="e85cc-125">Określa godzinę, o której muszą być uruchomione maszyny wirtualne laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e85cc-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85cc-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e85cc-126">-Confirm</span></span>
<span data-ttu-id="e85cc-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e85cc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e85cc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e85cc-128">-WhatIf</span></span>
<span data-ttu-id="e85cc-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e85cc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e85cc-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e85cc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e85cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85cc-131">CommonParameters</span></span>
<span data-ttu-id="e85cc-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e85cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85cc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e85cc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85cc-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e85cc-134">INPUTS</span></span>

### <span data-ttu-id="e85cc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e85cc-135">System.String</span></span>

## <span data-ttu-id="e85cc-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e85cc-136">OUTPUTS</span></span>

### <span data-ttu-id="e85cc-137">Microsoft. Azure. Commands. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="e85cc-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="e85cc-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e85cc-138">NOTES</span></span>

## <span data-ttu-id="e85cc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e85cc-139">RELATED LINKS</span></span>

[<span data-ttu-id="e85cc-140">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="e85cc-140">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


