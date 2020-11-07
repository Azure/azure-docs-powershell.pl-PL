---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 76cc8117458db23f947a998d29de09a900bb6d42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716961"
---
# <span data-ttu-id="62a5d-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="62a5d-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="62a5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="62a5d-103">Modyfikuje harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="62a5d-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62a5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62a5d-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62a5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="62a5d-106">Polecenie cmdlet **Set-AzureRmAutomationSchedule** modyfikuje harmonogram w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="62a5d-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="62a5d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62a5d-107">EXAMPLES</span></span>

### <span data-ttu-id="62a5d-108">Przykład 1: modyfikowanie harmonogramu</span><span class="sxs-lookup"><span data-stu-id="62a5d-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="62a5d-109">To polecenie modyfikuje opis harmonogramu o nazwie Schedule01.</span><span class="sxs-lookup"><span data-stu-id="62a5d-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="62a5d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62a5d-110">PARAMETERS</span></span>

### <span data-ttu-id="62a5d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="62a5d-111">-AutomationAccountName</span></span>
<span data-ttu-id="62a5d-112">Określa nazwę konta automatyzacji, dla którego jest modyfikowany harmonogram za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a5d-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="62a5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a5d-113">-DefaultProfile</span></span>
<span data-ttu-id="62a5d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="62a5d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62a5d-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="62a5d-115">-Description</span></span>
<span data-ttu-id="62a5d-116">Określa opis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="62a5d-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a5d-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="62a5d-117">-IsEnabled</span></span>
<span data-ttu-id="62a5d-118">Określa, czy to polecenie cmdlet włącza harmonogram.</span><span class="sxs-lookup"><span data-stu-id="62a5d-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a5d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62a5d-119">-Name</span></span>
<span data-ttu-id="62a5d-120">Określa nazwę harmonogramu modyfikowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a5d-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a5d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a5d-121">-ResourceGroupName</span></span>
<span data-ttu-id="62a5d-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje harmonogram.</span><span class="sxs-lookup"><span data-stu-id="62a5d-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="62a5d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a5d-123">CommonParameters</span></span>
<span data-ttu-id="62a5d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a5d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a5d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62a5d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a5d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62a5d-126">INPUTS</span></span>

### <span data-ttu-id="62a5d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="62a5d-127">System.String</span></span>

### <span data-ttu-id="62a5d-128">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="62a5d-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="62a5d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62a5d-129">OUTPUTS</span></span>

### <span data-ttu-id="62a5d-130">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="62a5d-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="62a5d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62a5d-131">NOTES</span></span>

## <span data-ttu-id="62a5d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62a5d-132">RELATED LINKS</span></span>

[<span data-ttu-id="62a5d-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="62a5d-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="62a5d-134">Nowe — AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="62a5d-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="62a5d-135">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="62a5d-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


