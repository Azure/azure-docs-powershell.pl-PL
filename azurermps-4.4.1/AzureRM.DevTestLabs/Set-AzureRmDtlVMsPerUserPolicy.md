---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: b3790105f2404cc7bf50ef1200ce0978e8f0b15d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551027"
---
# <span data-ttu-id="79849-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="79849-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="79849-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79849-102">SYNOPSIS</span></span>
<span data-ttu-id="79849-103">Ustawia zasady dotyczące maszyn wirtualnych według użytkowników laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="79849-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79849-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79849-104">SYNTAX</span></span>

### <span data-ttu-id="79849-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="79849-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79849-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="79849-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79849-107">Opis</span><span class="sxs-lookup"><span data-stu-id="79849-107">DESCRIPTION</span></span>
<span data-ttu-id="79849-108">Polecenie cmdlet **Set-AzureRmDtlVMsPerUserPolicy** ustawia zasady dotyczące maszyn wirtualnych według użytkowników laboratorium, które ustawia maksymalną liczbę maszyn wirtualnych dozwolonych dla jednego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="79849-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="79849-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="79849-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="79849-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79849-110">EXAMPLES</span></span>

## <span data-ttu-id="79849-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79849-111">PARAMETERS</span></span>

### <span data-ttu-id="79849-112">-Disable</span><span class="sxs-lookup"><span data-stu-id="79849-112">-Disable</span></span>
<span data-ttu-id="79849-113">Wskazuje, że to polecenie cmdlet wyłącza zasady dla laboratorium.</span><span class="sxs-lookup"><span data-stu-id="79849-113">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="79849-114">-Enable</span><span class="sxs-lookup"><span data-stu-id="79849-114">-Enable</span></span>
<span data-ttu-id="79849-115">Wskazuje, że to polecenie cmdlet włącza zasady dla laboratorium.</span><span class="sxs-lookup"><span data-stu-id="79849-115">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="79849-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="79849-116">-LabName</span></span>
<span data-ttu-id="79849-117">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia zasady maszyny wirtualnej na użytkownika.</span><span class="sxs-lookup"><span data-stu-id="79849-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="79849-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="79849-118">-MaxVMs</span></span>
<span data-ttu-id="79849-119">Określa maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="79849-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="79849-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79849-120">-ResourceGroupName</span></span>
<span data-ttu-id="79849-121">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="79849-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="79849-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79849-122">-Confirm</span></span>
<span data-ttu-id="79849-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79849-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79849-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79849-124">-WhatIf</span></span>
<span data-ttu-id="79849-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79849-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79849-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79849-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79849-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79849-127">-DefaultProfile</span></span>
<span data-ttu-id="79849-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79849-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79849-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79849-129">CommonParameters</span></span>
<span data-ttu-id="79849-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79849-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79849-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79849-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79849-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79849-132">INPUTS</span></span>

## <span data-ttu-id="79849-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79849-133">OUTPUTS</span></span>

### <span data-ttu-id="79849-134">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="79849-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="79849-135">To polecenie cmdlet zwraca zasadę określającą maksymalną liczbę maszyn wirtualnych, które mogą zostać utworzone przez użytkownika w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="79849-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="79849-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79849-136">NOTES</span></span>

## <span data-ttu-id="79849-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79849-137">RELATED LINKS</span></span>

[<span data-ttu-id="79849-138">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="79849-138">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


