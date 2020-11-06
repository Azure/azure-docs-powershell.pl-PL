---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: d812d66911c31297a2aaf4a32fd73562bc4ae9b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551035"
---
# <span data-ttu-id="eed42-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="eed42-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="eed42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eed42-102">SYNOPSIS</span></span>
<span data-ttu-id="eed42-103">Ustawia zasady automatycznego zamykania laboratoriów laboratorium DevTest.</span><span class="sxs-lookup"><span data-stu-id="eed42-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eed42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eed42-104">SYNTAX</span></span>

### <span data-ttu-id="eed42-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="eed42-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eed42-106">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="eed42-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eed42-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eed42-107">DESCRIPTION</span></span>
<span data-ttu-id="eed42-108">Polecenie cmdlet **Set-AzureRmDtlAutoShutdownPolicy** ustawia zasady automatycznego zamykania laboratorium, które powoduje automatyczne zamknięcie wszystkich maszyn wirtualnych w laboratorium o określonej porze dnia.</span><span class="sxs-lookup"><span data-stu-id="eed42-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="eed42-109">W poleceniu cmdlet jest używana określona grupa zasobów i nazwa laboratorium w celu ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="eed42-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="eed42-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eed42-110">EXAMPLES</span></span>

## <span data-ttu-id="eed42-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eed42-111">PARAMETERS</span></span>

### <span data-ttu-id="eed42-112">-Disable</span><span class="sxs-lookup"><span data-stu-id="eed42-112">-Disable</span></span>
<span data-ttu-id="eed42-113">Wskazuje, że polecenie cmdlet wyłącza zasady w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="eed42-113">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="eed42-114">-Enable</span><span class="sxs-lookup"><span data-stu-id="eed42-114">-Enable</span></span>
<span data-ttu-id="eed42-115">Wskazuje, że polecenie cmdlet włącza zasady w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="eed42-115">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="eed42-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="eed42-116">-LabName</span></span>
<span data-ttu-id="eed42-117">Określa nazwę laboratorium, dla którego to polecenie cmdlet ustawia zasadę automatycznego zamykania.</span><span class="sxs-lookup"><span data-stu-id="eed42-117">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="eed42-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed42-118">-ResourceGroupName</span></span>
<span data-ttu-id="eed42-119">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="eed42-119">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="eed42-120">-Time (czas)</span><span class="sxs-lookup"><span data-stu-id="eed42-120">-Time</span></span>
<span data-ttu-id="eed42-121">Określa czas (w postaci obiektu **DateTime** ) dla sytuacji, gdy maszyny wirtualne w laboratorium muszą zostać zamknięte.</span><span class="sxs-lookup"><span data-stu-id="eed42-121">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

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

### <span data-ttu-id="eed42-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eed42-122">-Confirm</span></span>
<span data-ttu-id="eed42-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed42-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed42-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed42-124">-WhatIf</span></span>
<span data-ttu-id="eed42-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed42-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed42-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eed42-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed42-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed42-127">-DefaultProfile</span></span>
<span data-ttu-id="eed42-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eed42-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eed42-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed42-129">CommonParameters</span></span>
<span data-ttu-id="eed42-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed42-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed42-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed42-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed42-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eed42-132">INPUTS</span></span>

## <span data-ttu-id="eed42-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eed42-133">OUTPUTS</span></span>

### <span data-ttu-id="eed42-134">Microsoft. Azure. Commands. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="eed42-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="eed42-135">To polecenie cmdlet zwraca harmonogram, który określa, kiedy maszyny wirtualne w laboratorium muszą zostać zamknięte.</span><span class="sxs-lookup"><span data-stu-id="eed42-135">This cmdlet returns the schedule which specifies when the virtual machines in the lab must shut down.</span></span>

## <span data-ttu-id="eed42-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eed42-136">NOTES</span></span>

## <span data-ttu-id="eed42-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eed42-137">RELATED LINKS</span></span>

[<span data-ttu-id="eed42-138">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="eed42-138">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)


