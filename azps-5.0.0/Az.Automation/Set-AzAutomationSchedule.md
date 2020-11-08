---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232129"
---
# <span data-ttu-id="a6937-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a6937-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="a6937-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6937-102">SYNOPSIS</span></span>
<span data-ttu-id="a6937-103">Modyfikuje harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a6937-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="a6937-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6937-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6937-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6937-105">DESCRIPTION</span></span>
<span data-ttu-id="a6937-106">Polecenie cmdlet **Set-AzAutomationSchedule** modyfikuje harmonogram w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a6937-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="a6937-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6937-107">EXAMPLES</span></span>

### <span data-ttu-id="a6937-108">Przykład 1: modyfikowanie harmonogramu</span><span class="sxs-lookup"><span data-stu-id="a6937-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a6937-109">To polecenie modyfikuje opis harmonogramu o nazwie Schedule01.</span><span class="sxs-lookup"><span data-stu-id="a6937-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="a6937-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6937-110">PARAMETERS</span></span>

### <span data-ttu-id="a6937-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6937-111">-AutomationAccountName</span></span>
<span data-ttu-id="a6937-112">Określa nazwę konta automatyzacji, dla którego jest modyfikowany harmonogram za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6937-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="a6937-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6937-113">-DefaultProfile</span></span>
<span data-ttu-id="a6937-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a6937-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6937-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="a6937-115">-Description</span></span>
<span data-ttu-id="a6937-116">Określa opis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="a6937-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="a6937-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a6937-117">-IsEnabled</span></span>
<span data-ttu-id="a6937-118">Określa, czy to polecenie cmdlet włącza harmonogram.</span><span class="sxs-lookup"><span data-stu-id="a6937-118">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="a6937-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6937-119">-Name</span></span>
<span data-ttu-id="a6937-120">Określa nazwę harmonogramu modyfikowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6937-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a6937-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6937-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6937-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje harmonogram.</span><span class="sxs-lookup"><span data-stu-id="a6937-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="a6937-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6937-123">CommonParameters</span></span>
<span data-ttu-id="a6937-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6937-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6937-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6937-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6937-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6937-126">INPUTS</span></span>

### <span data-ttu-id="a6937-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a6937-127">System.String</span></span>

### <span data-ttu-id="a6937-128">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a6937-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a6937-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6937-129">OUTPUTS</span></span>

### <span data-ttu-id="a6937-130">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="a6937-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="a6937-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6937-131">NOTES</span></span>

## <span data-ttu-id="a6937-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6937-132">RELATED LINKS</span></span>

[<span data-ttu-id="a6937-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a6937-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="a6937-134">Nowe — AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a6937-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="a6937-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a6937-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


