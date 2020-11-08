---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055037"
---
# <span data-ttu-id="15dc3-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="15dc3-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="15dc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15dc3-102">SYNOPSIS</span></span>

<span data-ttu-id="15dc3-103">Modyfikuje harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="15dc3-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="15dc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15dc3-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="15dc3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15dc3-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="15dc3-106">Polecenie cmdlet **Set-AzureAutomationSchedule** modyfikuje harmonogram w usłudze Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="15dc3-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="15dc3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="15dc3-108">Przykład 1: modyfikowanie harmonogramu</span><span class="sxs-lookup"><span data-stu-id="15dc3-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="15dc3-109">To polecenie modyfikuje opis harmonogramu o nazwie Schedule01.</span><span class="sxs-lookup"><span data-stu-id="15dc3-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="15dc3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15dc3-110">PARAMETERS</span></span>

### <span data-ttu-id="15dc3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="15dc3-111">-AutomationAccountName</span></span>
<span data-ttu-id="15dc3-112">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="15dc3-112">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dc3-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="15dc3-113">-Description</span></span>
<span data-ttu-id="15dc3-114">Określa opis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="15dc3-114">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dc3-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="15dc3-115">-IsEnabled</span></span>
<span data-ttu-id="15dc3-116">Wskazuje, czy harmonogram jest włączony.</span><span class="sxs-lookup"><span data-stu-id="15dc3-116">Indicates whether the schedule is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dc3-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15dc3-117">-Name</span></span>
<span data-ttu-id="15dc3-118">Określa nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="15dc3-118">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dc3-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="15dc3-119">-Profile</span></span>
<span data-ttu-id="15dc3-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15dc3-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15dc3-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="15dc3-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dc3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15dc3-122">CommonParameters</span></span>
<span data-ttu-id="15dc3-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15dc3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15dc3-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15dc3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15dc3-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15dc3-125">INPUTS</span></span>

## <span data-ttu-id="15dc3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15dc3-126">OUTPUTS</span></span>

### <span data-ttu-id="15dc3-127">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="15dc3-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="15dc3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15dc3-128">NOTES</span></span>

## <span data-ttu-id="15dc3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15dc3-129">RELATED LINKS</span></span>

[<span data-ttu-id="15dc3-130">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="15dc3-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="15dc3-131">Nowe — AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="15dc3-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="15dc3-132">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="15dc3-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


