---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054621"
---
# <span data-ttu-id="7629d-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7629d-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="7629d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7629d-102">SYNOPSIS</span></span>

<span data-ttu-id="7629d-103">Pobiera harmonogram usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7629d-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="7629d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7629d-104">SYNTAX</span></span>

### <span data-ttu-id="7629d-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7629d-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7629d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7629d-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7629d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7629d-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7629d-108">Polecenie cmdlet **Get-AzureAutomationSchedule** pobiera harmonogram usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7629d-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="7629d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7629d-109">EXAMPLES</span></span>

### <span data-ttu-id="7629d-110">Przykład 1: Uzyskaj harmonogram</span><span class="sxs-lookup"><span data-stu-id="7629d-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="7629d-111">To polecenie uzyskuje harmonogram o nazwie DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="7629d-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="7629d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7629d-112">PARAMETERS</span></span>

### <span data-ttu-id="7629d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7629d-113">-AutomationAccountName</span></span>
<span data-ttu-id="7629d-114">Określa nazwę konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7629d-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="7629d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7629d-115">-Name</span></span>
<span data-ttu-id="7629d-116">Określa nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="7629d-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7629d-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="7629d-117">-Profile</span></span>
<span data-ttu-id="7629d-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7629d-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7629d-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7629d-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7629d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7629d-120">CommonParameters</span></span>
<span data-ttu-id="7629d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7629d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7629d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7629d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7629d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7629d-123">INPUTS</span></span>

## <span data-ttu-id="7629d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7629d-124">OUTPUTS</span></span>

### <span data-ttu-id="7629d-125">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="7629d-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="7629d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7629d-126">NOTES</span></span>

## <span data-ttu-id="7629d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7629d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7629d-128">Nowe — AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7629d-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="7629d-129">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7629d-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="7629d-130">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7629d-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


