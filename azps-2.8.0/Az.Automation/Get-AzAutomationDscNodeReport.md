---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: a8d0244b9a26616e796a4e867a193da4ed3888d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706820"
---
# <span data-ttu-id="9f737-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="9f737-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="9f737-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f737-102">SYNOPSIS</span></span>
<span data-ttu-id="9f737-103">Umożliwia pobieranie raportów wysłanych z węzła DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9f737-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="9f737-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f737-104">SYNTAX</span></span>

### <span data-ttu-id="9f737-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9f737-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f737-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="9f737-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f737-107">ById</span><span class="sxs-lookup"><span data-stu-id="9f737-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f737-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9f737-108">DESCRIPTION</span></span>
<span data-ttu-id="9f737-109">Polecenie cmdlet **Get-AzAutomationDscNodeReport** pobiera raporty wysyłane z węzła APS (Konfiguracja stanu żądanego) do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9f737-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="9f737-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f737-110">EXAMPLES</span></span>

### <span data-ttu-id="9f737-111">Przykład 1. pobieranie wszystkich raportów dla węzła DSC</span><span class="sxs-lookup"><span data-stu-id="9f737-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="9f737-112">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9f737-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="9f737-113">Polecenie zapisuje ten obiekt w zmiennej $Node.</span><span class="sxs-lookup"><span data-stu-id="9f737-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="9f737-114">Drugie polecenie pobiera metadane wszystkich raportów wysyłanych z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9f737-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="9f737-115">Polecenie określa węzeł za pomocą właściwości **Identyfikator** obiektu $Node.</span><span class="sxs-lookup"><span data-stu-id="9f737-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="9f737-116">Przykład 2: uzyskiwanie raportu dla węzła DSC według identyfikatora raportu</span><span class="sxs-lookup"><span data-stu-id="9f737-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="9f737-117">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9f737-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="9f737-118">Polecenie zapisuje ten obiekt w zmiennej $Node.</span><span class="sxs-lookup"><span data-stu-id="9f737-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="9f737-119">Drugie polecenie pobiera metadane dla raportu określonego IDENTYFIKATORem wysłanym z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9f737-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9f737-120">Przykład 3: uzyskiwanie najnowszego raportu dla węzła DSC</span><span class="sxs-lookup"><span data-stu-id="9f737-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="9f737-121">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9f737-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="9f737-122">Polecenie zapisuje ten obiekt w zmiennej $Node.</span><span class="sxs-lookup"><span data-stu-id="9f737-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="9f737-123">Drugie polecenie pobiera metadane najnowszego raportu wysłanego z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9f737-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9f737-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f737-124">PARAMETERS</span></span>

### <span data-ttu-id="9f737-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f737-125">-AutomationAccountName</span></span>
<span data-ttu-id="9f737-126">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9f737-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="9f737-127">To polecenie cmdlet powoduje wyeksportowanie raportów dla węzła DSC należącego do konta, które jest określone przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9f737-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f737-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f737-128">-DefaultProfile</span></span>
<span data-ttu-id="9f737-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9f737-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f737-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9f737-130">-EndTime</span></span>
<span data-ttu-id="9f737-131">Określa godzinę zakończenia.</span><span class="sxs-lookup"><span data-stu-id="9f737-131">Specifies an end time.</span></span>
<span data-ttu-id="9f737-132">To polecenie cmdlet umożliwia pobieranie raportów, które zostały odebrane przed upływem tego czasu.</span><span class="sxs-lookup"><span data-stu-id="9f737-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f737-133">-ID</span><span class="sxs-lookup"><span data-stu-id="9f737-133">-Id</span></span>
<span data-ttu-id="9f737-134">Określa unikatowy identyfikator raportu węzła DSC dla tego polecenia cmdlet, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="9f737-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f737-135">-Najnowsze</span><span class="sxs-lookup"><span data-stu-id="9f737-135">-Latest</span></span>
<span data-ttu-id="9f737-136">Wskazuje, że ten aplet polecenia pobiera najnowszy raport DSC tylko dla określonego węzła.</span><span class="sxs-lookup"><span data-stu-id="9f737-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f737-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="9f737-137">-NodeId</span></span>
<span data-ttu-id="9f737-138">Określa unikatowy identyfikator węzła DSC, dla którego ten aplet polecenia pobiera raporty.</span><span class="sxs-lookup"><span data-stu-id="9f737-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="9f737-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f737-139">-ResourceGroupName</span></span>
<span data-ttu-id="9f737-140">Określa nazwę grupy zasobów zawierającej węzeł DSC, dla którego ten aplet polecenia pobiera raporty.</span><span class="sxs-lookup"><span data-stu-id="9f737-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="9f737-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9f737-141">-StartTime</span></span>
<span data-ttu-id="9f737-142">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="9f737-142">Specifies a start time.</span></span>
<span data-ttu-id="9f737-143">To polecenie cmdlet umożliwia pobieranie raportów, które zostały odebrane po upływie tego czasu.</span><span class="sxs-lookup"><span data-stu-id="9f737-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f737-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f737-144">CommonParameters</span></span>
<span data-ttu-id="9f737-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f737-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f737-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f737-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f737-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f737-147">INPUTS</span></span>

### <span data-ttu-id="9f737-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9f737-148">System.Guid</span></span>

### <span data-ttu-id="9f737-149">System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9f737-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9f737-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9f737-150">System.String</span></span>

## <span data-ttu-id="9f737-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f737-151">OUTPUTS</span></span>

### <span data-ttu-id="9f737-152">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="9f737-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="9f737-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f737-153">NOTES</span></span>

## <span data-ttu-id="9f737-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f737-154">RELATED LINKS</span></span>

[<span data-ttu-id="9f737-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f737-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="9f737-156">Eksportowanie — AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="9f737-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


