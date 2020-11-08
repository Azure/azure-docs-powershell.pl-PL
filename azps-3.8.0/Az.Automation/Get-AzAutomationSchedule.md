---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051634"
---
# <span data-ttu-id="6f41e-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6f41e-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="6f41e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f41e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f41e-103">Pobiera harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="6f41e-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="6f41e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f41e-104">SYNTAX</span></span>

### <span data-ttu-id="6f41e-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6f41e-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f41e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f41e-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f41e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6f41e-107">DESCRIPTION</span></span>
<span data-ttu-id="6f41e-108">Polecenie cmdlet **Get-AzAutomationSchedule** pobiera harmonogram usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6f41e-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="6f41e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f41e-109">EXAMPLES</span></span>

### <span data-ttu-id="6f41e-110">Przykład 1: Uzyskaj harmonogram</span><span class="sxs-lookup"><span data-stu-id="6f41e-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6f41e-111">To polecenie uzyskuje harmonogram o nazwie DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="6f41e-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="6f41e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f41e-112">PARAMETERS</span></span>

### <span data-ttu-id="6f41e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f41e-113">-AutomationAccountName</span></span>
<span data-ttu-id="6f41e-114">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet uzyskuje harmonogram.</span><span class="sxs-lookup"><span data-stu-id="6f41e-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="6f41e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f41e-115">-DefaultProfile</span></span>
<span data-ttu-id="6f41e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6f41e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f41e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f41e-117">-Name</span></span>
<span data-ttu-id="6f41e-118">Określa nazwę harmonogramu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f41e-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f41e-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f41e-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera harmonogram.</span><span class="sxs-lookup"><span data-stu-id="6f41e-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="6f41e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f41e-121">CommonParameters</span></span>
<span data-ttu-id="6f41e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f41e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f41e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f41e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f41e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f41e-124">INPUTS</span></span>

### <span data-ttu-id="6f41e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6f41e-125">System.String</span></span>

## <span data-ttu-id="6f41e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f41e-126">OUTPUTS</span></span>

### <span data-ttu-id="6f41e-127">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="6f41e-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="6f41e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f41e-128">NOTES</span></span>

## <span data-ttu-id="6f41e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f41e-129">RELATED LINKS</span></span>

[<span data-ttu-id="6f41e-130">Nowe — AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6f41e-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="6f41e-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6f41e-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="6f41e-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6f41e-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


