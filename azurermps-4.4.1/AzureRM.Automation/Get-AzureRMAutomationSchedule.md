---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 1252864be8e55638ec5e982bd075aec647b68a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554234"
---
# <span data-ttu-id="476e6-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="476e6-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="476e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="476e6-102">SYNOPSIS</span></span>
<span data-ttu-id="476e6-103">Pobiera harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="476e6-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="476e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="476e6-104">SYNTAX</span></span>

### <span data-ttu-id="476e6-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="476e6-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="476e6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="476e6-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="476e6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="476e6-107">DESCRIPTION</span></span>
<span data-ttu-id="476e6-108">Polecenie cmdlet **Get-AzureRmAutomationSchedule** pobiera harmonogram usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="476e6-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="476e6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="476e6-109">EXAMPLES</span></span>

### <span data-ttu-id="476e6-110">Przykład 1: Uzyskaj harmonogram</span><span class="sxs-lookup"><span data-stu-id="476e6-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="476e6-111">To polecenie uzyskuje harmonogram o nazwie DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="476e6-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="476e6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="476e6-112">PARAMETERS</span></span>

### <span data-ttu-id="476e6-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="476e6-113">-AutomationAccountName</span></span>
<span data-ttu-id="476e6-114">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet uzyskuje harmonogram.</span><span class="sxs-lookup"><span data-stu-id="476e6-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="476e6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="476e6-115">-Name</span></span>
<span data-ttu-id="476e6-116">Określa nazwę harmonogramu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="476e6-116">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="476e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="476e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="476e6-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera harmonogram.</span><span class="sxs-lookup"><span data-stu-id="476e6-118">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="476e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476e6-119">-DefaultProfile</span></span>
<span data-ttu-id="476e6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="476e6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="476e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476e6-121">CommonParameters</span></span>
<span data-ttu-id="476e6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476e6-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476e6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476e6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="476e6-124">INPUTS</span></span>

## <span data-ttu-id="476e6-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="476e6-125">OUTPUTS</span></span>

### <span data-ttu-id="476e6-126">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="476e6-126">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="476e6-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="476e6-127">NOTES</span></span>

## <span data-ttu-id="476e6-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="476e6-128">RELATED LINKS</span></span>

[<span data-ttu-id="476e6-129">Nowe — AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="476e6-129">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="476e6-130">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="476e6-130">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="476e6-131">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="476e6-131">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


