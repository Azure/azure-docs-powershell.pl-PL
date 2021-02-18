---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: cc7beb921e09a2cdf1568e9cb693dd01f059e562
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239634"
---
# <span data-ttu-id="68e95-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="68e95-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="68e95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68e95-102">SYNOPSIS</span></span>
<span data-ttu-id="68e95-103">Pobiera raporty wysyłane z węzła DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="68e95-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="68e95-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="68e95-104">SYNTAX</span></span>

### <span data-ttu-id="68e95-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="68e95-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68e95-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="68e95-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68e95-107">ById</span><span class="sxs-lookup"><span data-stu-id="68e95-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68e95-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="68e95-108">DESCRIPTION</span></span>
<span data-ttu-id="68e95-109">Polecenie **cmdlet Get-AzAutomationDscNodeReport** pobiera raporty wysyłane z węzła APS Desired State Configuration (DSC) do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="68e95-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="68e95-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="68e95-110">EXAMPLES</span></span>

### <span data-ttu-id="68e95-111">Przykład 1. Uzyskiwanie wszystkich raportów dla węzła DSC</span><span class="sxs-lookup"><span data-stu-id="68e95-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="68e95-112">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68e95-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="68e95-113">Polecenie przechowuje ten obiekt w $Node zmienną.</span><span class="sxs-lookup"><span data-stu-id="68e95-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="68e95-114">Drugie polecenie pobiera metadane dla wszystkich raportów wysyłanych z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68e95-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="68e95-115">To polecenie określa węzeł przy użyciu właściwości **Id** $Node obiektu.</span><span class="sxs-lookup"><span data-stu-id="68e95-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="68e95-116">Przykład 2. Uzyskiwanie raportu dla węzła DSC według identyfikatora raportu</span><span class="sxs-lookup"><span data-stu-id="68e95-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="68e95-117">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68e95-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="68e95-118">Polecenie przechowuje ten obiekt w $Node zmienną.</span><span class="sxs-lookup"><span data-stu-id="68e95-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="68e95-119">Drugie polecenie pobiera metadane dla raportu wskazanego przez określony identyfikator wysyłany z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68e95-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="68e95-120">Przykład 3. Uzyskiwanie najnowszego raportu dla węzła DSC</span><span class="sxs-lookup"><span data-stu-id="68e95-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="68e95-121">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68e95-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="68e95-122">Polecenie przechowuje ten obiekt w $Node zmienną.</span><span class="sxs-lookup"><span data-stu-id="68e95-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="68e95-123">Drugie polecenie pobiera metadane dla najnowszego raportu wysyłanego z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68e95-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="68e95-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68e95-124">PARAMETERS</span></span>

### <span data-ttu-id="68e95-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="68e95-125">-AutomationAccountName</span></span>
<span data-ttu-id="68e95-126">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="68e95-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="68e95-127">To polecenie cmdlet eksportuje raporty dla węzła DSC należącego do konta, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="68e95-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="68e95-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e95-128">-DefaultProfile</span></span>
<span data-ttu-id="68e95-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="68e95-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68e95-130">- EndTime</span><span class="sxs-lookup"><span data-stu-id="68e95-130">-EndTime</span></span>
<span data-ttu-id="68e95-131">Określa czas zakończenia.</span><span class="sxs-lookup"><span data-stu-id="68e95-131">Specifies an end time.</span></span>
<span data-ttu-id="68e95-132">To polecenie cmdlet pobiera raporty o automatyzacji odebrane przed tym terminem.</span><span class="sxs-lookup"><span data-stu-id="68e95-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="68e95-133">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="68e95-133">-Id</span></span>
<span data-ttu-id="68e95-134">Określa unikatowy identyfikator raportu węzła DSC dla tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68e95-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="68e95-135">— najnowsza wersja</span><span class="sxs-lookup"><span data-stu-id="68e95-135">-Latest</span></span>
<span data-ttu-id="68e95-136">Wskazuje, że to polecenie cmdlet pobiera najnowszy raport DSC tylko dla określonego węzła.</span><span class="sxs-lookup"><span data-stu-id="68e95-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="68e95-137">- NodeId</span><span class="sxs-lookup"><span data-stu-id="68e95-137">-NodeId</span></span>
<span data-ttu-id="68e95-138">Określa unikatowy identyfikator węzła DSC, dla którego to polecenie cmdlet pobiera raporty.</span><span class="sxs-lookup"><span data-stu-id="68e95-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="68e95-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e95-139">-ResourceGroupName</span></span>
<span data-ttu-id="68e95-140">Określa nazwę grupy zasobów zawierającej węzeł DSC, dla którego to polecenie cmdlet pobiera raporty.</span><span class="sxs-lookup"><span data-stu-id="68e95-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="68e95-141">— StartTime</span><span class="sxs-lookup"><span data-stu-id="68e95-141">-StartTime</span></span>
<span data-ttu-id="68e95-142">Określa czas rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="68e95-142">Specifies a start time.</span></span>
<span data-ttu-id="68e95-143">To polecenie cmdlet pobiera raporty, które po tym czasie otrzymano automatyzację.</span><span class="sxs-lookup"><span data-stu-id="68e95-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="68e95-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e95-144">CommonParameters</span></span>
<span data-ttu-id="68e95-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e95-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e95-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e95-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e95-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68e95-147">INPUTS</span></span>

### <span data-ttu-id="68e95-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="68e95-148">System.Guid</span></span>

### <span data-ttu-id="68e95-149">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="68e95-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="68e95-150">System.String</span><span class="sxs-lookup"><span data-stu-id="68e95-150">System.String</span></span>

## <span data-ttu-id="68e95-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68e95-151">OUTPUTS</span></span>

### <span data-ttu-id="68e95-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="68e95-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="68e95-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="68e95-153">NOTES</span></span>

## <span data-ttu-id="68e95-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68e95-154">RELATED LINKS</span></span>

[<span data-ttu-id="68e95-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="68e95-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="68e95-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="68e95-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


