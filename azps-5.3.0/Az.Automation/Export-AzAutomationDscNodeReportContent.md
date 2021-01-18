---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502400"
---
# <span data-ttu-id="2dc3f-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="2dc3f-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="2dc3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dc3f-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc3f-103">Eksportuje nieprzetworzoną zawartość raportu konfiguracji DSC wysłaną z węzła DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="2dc3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dc3f-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dc3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2dc3f-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc3f-106">Polecenie cmdlet **Export-AzAutomationDscNodeReportContent** wyeksportuje nieprzetworzoną zawartość raportu konfiguracji stanu programu APS (DSC).</span><span class="sxs-lookup"><span data-stu-id="2dc3f-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="2dc3f-107">Węzeł DSC wysyła raport konfiguracji DSC do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="2dc3f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dc3f-108">EXAMPLES</span></span>

### <span data-ttu-id="2dc3f-109">Przykład 1. Eksportowanie raportu z węzła DSC</span><span class="sxs-lookup"><span data-stu-id="2dc3f-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="2dc3f-110">Ten zestaw poleceń powoduje wyeksportowanie najnowszego raportu z węzła DSC o nazwie Computer14 na komputer.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="2dc3f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dc3f-111">PARAMETERS</span></span>

### <span data-ttu-id="2dc3f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2dc3f-112">-AutomationAccountName</span></span>
<span data-ttu-id="2dc3f-113">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="2dc3f-114">To polecenie cmdlet eksportuje zawartość raportu dla węzła DSC należącego do konta automatyzacji, które jest określone przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="2dc3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc3f-115">-DefaultProfile</span></span>
<span data-ttu-id="2dc3f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2dc3f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dc3f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2dc3f-117">-Force</span></span>
<span data-ttu-id="2dc3f-118">Wskazuje, że to polecenie cmdlet Zamienia istniejący plik lokalny na nowy plik o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc3f-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="2dc3f-119">-NodeId</span></span>
<span data-ttu-id="2dc3f-120">Określa unikatowy identyfikator węzła DSC, dla którego to polecenie cmdlet eksportuje zawartość raportu.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dc3f-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="2dc3f-121">-OutputFolder</span></span>
<span data-ttu-id="2dc3f-122">Określa folder wyjściowy, w którym to polecenie cmdlet eksportuje zawartość raportu.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="2dc3f-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="2dc3f-123">-ReportId</span></span>
<span data-ttu-id="2dc3f-124">Określa unikatowy identyfikator raportu węzła DSC, który jest eksportowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dc3f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc3f-125">-ResourceGroupName</span></span>
<span data-ttu-id="2dc3f-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2dc3f-127">To polecenie cmdlet umożliwia wyeksportowanie zawartości raportu dotyczącego węzła DSC należącego do grupy zasobów, którą to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="2dc3f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dc3f-128">-Confirm</span></span>
<span data-ttu-id="2dc3f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc3f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc3f-130">-WhatIf</span></span>
<span data-ttu-id="2dc3f-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dc3f-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dc3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc3f-133">CommonParameters</span></span>
<span data-ttu-id="2dc3f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc3f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc3f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc3f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dc3f-136">INPUTS</span></span>

### <span data-ttu-id="2dc3f-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2dc3f-137">System.Guid</span></span>

### <span data-ttu-id="2dc3f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2dc3f-138">System.String</span></span>

## <span data-ttu-id="2dc3f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dc3f-139">OUTPUTS</span></span>

### <span data-ttu-id="2dc3f-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="2dc3f-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="2dc3f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dc3f-141">NOTES</span></span>

## <span data-ttu-id="2dc3f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dc3f-142">RELATED LINKS</span></span>

[<span data-ttu-id="2dc3f-143">Eksportowanie — AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="2dc3f-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="2dc3f-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2dc3f-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="2dc3f-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="2dc3f-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


