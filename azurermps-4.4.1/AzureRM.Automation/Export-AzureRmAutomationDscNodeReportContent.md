---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 23c17a0614a28a571b58e19ff2556c45679e6c82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547164"
---
# <span data-ttu-id="1994e-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="1994e-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="1994e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1994e-102">SYNOPSIS</span></span>
<span data-ttu-id="1994e-103">Eksportuje nieprzetworzoną zawartość raportu konfiguracji DSC wysłaną z węzła DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1994e-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1994e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1994e-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1994e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1994e-105">DESCRIPTION</span></span>
<span data-ttu-id="1994e-106">Polecenie cmdlet **Export-AzureRmAutomationDscNodeReportContent** wyeksportuje nieprzetworzoną zawartość raportu konfiguracji stanu programu APS (DSC).</span><span class="sxs-lookup"><span data-stu-id="1994e-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="1994e-107">Węzeł DSC wysyła raport konfiguracji DSC do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1994e-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="1994e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1994e-108">EXAMPLES</span></span>

### <span data-ttu-id="1994e-109">Przykład 1. Eksportowanie raportu z węzła DSC</span><span class="sxs-lookup"><span data-stu-id="1994e-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="1994e-110">Ten zestaw poleceń powoduje wyeksportowanie najnowszego raportu z węzła DSC o nazwie Computer14 na komputer.</span><span class="sxs-lookup"><span data-stu-id="1994e-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="1994e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1994e-111">PARAMETERS</span></span>

### <span data-ttu-id="1994e-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1994e-112">-AutomationAccountName</span></span>
<span data-ttu-id="1994e-113">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1994e-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="1994e-114">To polecenie cmdlet eksportuje zawartość raportu dla węzła DSC należącego do konta automatyzacji, które jest określone przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1994e-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="1994e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1994e-115">-Force</span></span>
<span data-ttu-id="1994e-116">Wskazuje, że to polecenie cmdlet Zamienia istniejący plik lokalny na nowy plik o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="1994e-116">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="1994e-117">-NodeId</span><span class="sxs-lookup"><span data-stu-id="1994e-117">-NodeId</span></span>
<span data-ttu-id="1994e-118">Określa unikatowy identyfikator węzła DSC, dla którego to polecenie cmdlet eksportuje zawartość raportu.</span><span class="sxs-lookup"><span data-stu-id="1994e-118">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="1994e-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1994e-119">-OutputFolder</span></span>
<span data-ttu-id="1994e-120">Określa folder wyjściowy, w którym to polecenie cmdlet eksportuje zawartość raportu.</span><span class="sxs-lookup"><span data-stu-id="1994e-120">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="1994e-121">-ReportId</span><span class="sxs-lookup"><span data-stu-id="1994e-121">-ReportId</span></span>
<span data-ttu-id="1994e-122">Określa unikatowy identyfikator raportu węzła DSC, który jest eksportowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1994e-122">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="1994e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1994e-123">-ResourceGroupName</span></span>
<span data-ttu-id="1994e-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1994e-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1994e-125">To polecenie cmdlet umożliwia wyeksportowanie zawartości raportu dotyczącego węzła DSC należącego do grupy zasobów, którą to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="1994e-125">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="1994e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1994e-126">-Confirm</span></span>
<span data-ttu-id="1994e-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1994e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1994e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1994e-128">-WhatIf</span></span>
<span data-ttu-id="1994e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1994e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1994e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1994e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1994e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1994e-131">-DefaultProfile</span></span>
<span data-ttu-id="1994e-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1994e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1994e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1994e-133">CommonParameters</span></span>
<span data-ttu-id="1994e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1994e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1994e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1994e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1994e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1994e-136">INPUTS</span></span>

## <span data-ttu-id="1994e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1994e-137">OUTPUTS</span></span>

### <span data-ttu-id="1994e-138">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1994e-138">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="1994e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1994e-139">NOTES</span></span>

## <span data-ttu-id="1994e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1994e-140">RELATED LINKS</span></span>

[<span data-ttu-id="1994e-141">Eksportowanie — AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="1994e-141">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="1994e-142">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1994e-142">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="1994e-143">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="1994e-143">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


