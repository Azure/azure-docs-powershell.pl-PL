---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: b311554fa5aeeae67829055506b85766fd6f9670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548244"
---
# <span data-ttu-id="d513b-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d513b-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="d513b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d513b-102">SYNOPSIS</span></span>
<span data-ttu-id="d513b-103">Modyfikuje harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d513b-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d513b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d513b-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d513b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d513b-105">DESCRIPTION</span></span>
<span data-ttu-id="d513b-106">Polecenie cmdlet **Set-AzureRmAutomationSchedule** modyfikuje harmonogram w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d513b-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="d513b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d513b-107">EXAMPLES</span></span>

### <span data-ttu-id="d513b-108">Przykład 1: modyfikowanie harmonogramu</span><span class="sxs-lookup"><span data-stu-id="d513b-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d513b-109">To polecenie modyfikuje opis harmonogramu o nazwie Schedule01.</span><span class="sxs-lookup"><span data-stu-id="d513b-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="d513b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d513b-110">PARAMETERS</span></span>

### <span data-ttu-id="d513b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d513b-111">-AutomationAccountName</span></span>
<span data-ttu-id="d513b-112">Określa nazwę konta automatyzacji, dla którego jest modyfikowany harmonogram za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d513b-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="d513b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d513b-113">-DefaultProfile</span></span>
<span data-ttu-id="d513b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d513b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d513b-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="d513b-115">-Description</span></span>
<span data-ttu-id="d513b-116">Określa opis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d513b-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="d513b-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="d513b-117">-IsEnabled</span></span>
<span data-ttu-id="d513b-118">Określa, czy to polecenie cmdlet włącza harmonogram.</span><span class="sxs-lookup"><span data-stu-id="d513b-118">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="d513b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d513b-119">-Name</span></span>
<span data-ttu-id="d513b-120">Określa nazwę harmonogramu modyfikowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d513b-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d513b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d513b-121">-ResourceGroupName</span></span>
<span data-ttu-id="d513b-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje harmonogram.</span><span class="sxs-lookup"><span data-stu-id="d513b-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="d513b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d513b-123">CommonParameters</span></span>
<span data-ttu-id="d513b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d513b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d513b-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d513b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d513b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d513b-126">INPUTS</span></span>

### <span data-ttu-id="d513b-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d513b-127">None</span></span>
<span data-ttu-id="d513b-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d513b-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d513b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d513b-129">OUTPUTS</span></span>

### <span data-ttu-id="d513b-130">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="d513b-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="d513b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d513b-131">NOTES</span></span>

## <span data-ttu-id="d513b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d513b-132">RELATED LINKS</span></span>

[<span data-ttu-id="d513b-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d513b-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="d513b-134">Nowe — AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d513b-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="d513b-135">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d513b-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


