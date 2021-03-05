---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: c4006c13130cecb27c35d466c43cfd75583644b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975594"
---
# <span data-ttu-id="a816e-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="a816e-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="a816e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a816e-102">SYNOPSIS</span></span>
<span data-ttu-id="a816e-103">Eksportuje nieprzetworzone treści raportu DSC wysłanego z węzła DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a816e-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="a816e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a816e-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a816e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a816e-105">DESCRIPTION</span></span>
<span data-ttu-id="a816e-106">Polecenie **cmdlet Export-AzAutomationDscNodeReportContent** eksportuje nieprzetworzone treści raportu APS Desired State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="a816e-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="a816e-107">Węzeł DSC wysyła raport DSC do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a816e-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="a816e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a816e-108">EXAMPLES</span></span>

### <span data-ttu-id="a816e-109">Przykład 1. Eksportowanie raportu z węzła DSC</span><span class="sxs-lookup"><span data-stu-id="a816e-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="a816e-110">Ten zestaw poleceń eksportuje najnowszy raport z węzła DSC o nazwie Komputer14 na pulpit.</span><span class="sxs-lookup"><span data-stu-id="a816e-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="a816e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a816e-111">PARAMETERS</span></span>

### <span data-ttu-id="a816e-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a816e-112">-AutomationAccountName</span></span>
<span data-ttu-id="a816e-113">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a816e-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="a816e-114">To polecenie cmdlet eksportuje zawartość raportu dla węzła DSC, który należy do konta automatyzacji, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a816e-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="a816e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a816e-115">-DefaultProfile</span></span>
<span data-ttu-id="a816e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a816e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a816e-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a816e-117">-Force</span></span>
<span data-ttu-id="a816e-118">Wskazuje, że to polecenie cmdlet zastępuje istniejący plik lokalny nowym plikiem o takiej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="a816e-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="a816e-119">- NodeId</span><span class="sxs-lookup"><span data-stu-id="a816e-119">-NodeId</span></span>
<span data-ttu-id="a816e-120">Określa unikatowy identyfikator węzła DSC, dla którego to polecenie cmdlet eksportuje zawartość raportu.</span><span class="sxs-lookup"><span data-stu-id="a816e-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="a816e-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="a816e-121">-OutputFolder</span></span>
<span data-ttu-id="a816e-122">Określa folder wyjściowy, do którego to polecenie cmdlet eksportuje zawartość raportu.</span><span class="sxs-lookup"><span data-stu-id="a816e-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="a816e-123">- ReportId</span><span class="sxs-lookup"><span data-stu-id="a816e-123">-ReportId</span></span>
<span data-ttu-id="a816e-124">Określa unikatowy identyfikator raportu węzła DSC eksportowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a816e-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="a816e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a816e-125">-ResourceGroupName</span></span>
<span data-ttu-id="a816e-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a816e-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a816e-127">To polecenie cmdlet eksportuje zawartość raportu dla węzła DSC, który należy do grupy zasobów, której to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="a816e-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="a816e-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a816e-128">-Confirm</span></span>
<span data-ttu-id="a816e-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a816e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a816e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a816e-130">-WhatIf</span></span>
<span data-ttu-id="a816e-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a816e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a816e-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a816e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a816e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a816e-133">CommonParameters</span></span>
<span data-ttu-id="a816e-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a816e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a816e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a816e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a816e-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a816e-136">INPUTS</span></span>

### <span data-ttu-id="a816e-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a816e-137">System.Guid</span></span>

### <span data-ttu-id="a816e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a816e-138">System.String</span></span>

## <span data-ttu-id="a816e-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a816e-139">OUTPUTS</span></span>

### <span data-ttu-id="a816e-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="a816e-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="a816e-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a816e-141">NOTES</span></span>

## <span data-ttu-id="a816e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a816e-142">RELATED LINKS</span></span>

[<span data-ttu-id="a816e-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="a816e-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="a816e-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a816e-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="a816e-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="a816e-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


