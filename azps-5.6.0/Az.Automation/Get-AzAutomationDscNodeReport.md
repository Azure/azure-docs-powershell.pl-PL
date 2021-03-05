---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: bb88bc38f6102f18b4d45b3b80902886975e2628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987050"
---
# <span data-ttu-id="7ff3c-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="7ff3c-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="7ff3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ff3c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff3c-103">Pobiera raporty wysyłane z węzła DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="7ff3c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ff3c-104">SYNTAX</span></span>

### <span data-ttu-id="7ff3c-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7ff3c-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ff3c-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="7ff3c-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ff3c-107">ById</span><span class="sxs-lookup"><span data-stu-id="7ff3c-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ff3c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ff3c-108">DESCRIPTION</span></span>
<span data-ttu-id="7ff3c-109">Polecenie **cmdlet Get-AzAutomationDscNodeReport** pobiera raporty wysyłane z węzła APS Desired State Configuration (DSC) do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="7ff3c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ff3c-110">EXAMPLES</span></span>

### <span data-ttu-id="7ff3c-111">Przykład 1. Uzyskiwanie wszystkich raportów dla węzła DSC</span><span class="sxs-lookup"><span data-stu-id="7ff3c-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="7ff3c-112">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="7ff3c-113">Polecenie przechowuje ten obiekt w $Node zmienną.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="7ff3c-114">Drugie polecenie pobiera metadane dla wszystkich raportów wysyłanych z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="7ff3c-115">To polecenie określa węzeł przy użyciu właściwości **Id** $Node obiektu.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="7ff3c-116">Przykład 2. Uzyskiwanie raportu dla węzła DSC według identyfikatora raportu</span><span class="sxs-lookup"><span data-stu-id="7ff3c-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="7ff3c-117">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="7ff3c-118">Polecenie przechowuje ten obiekt w $Node zmienną.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="7ff3c-119">Drugie polecenie pobiera metadane dla raportu wskazanego przez określony identyfikator wysłany z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7ff3c-120">Przykład 3. Uzyskiwanie najnowszego raportu dla węzła DSC</span><span class="sxs-lookup"><span data-stu-id="7ff3c-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="7ff3c-121">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="7ff3c-122">Polecenie przechowuje ten obiekt w $Node zmienną.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="7ff3c-123">Drugie polecenie pobiera metadane dla najnowszego raportu wysyłanego z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7ff3c-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ff3c-124">PARAMETERS</span></span>

### <span data-ttu-id="7ff3c-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ff3c-125">-AutomationAccountName</span></span>
<span data-ttu-id="7ff3c-126">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="7ff3c-127">To polecenie cmdlet eksportuje raporty dla węzła DSC należącego do konta, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="7ff3c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff3c-128">-DefaultProfile</span></span>
<span data-ttu-id="7ff3c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7ff3c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ff3c-130">- EndTime</span><span class="sxs-lookup"><span data-stu-id="7ff3c-130">-EndTime</span></span>
<span data-ttu-id="7ff3c-131">Określa czas zakończenia.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-131">Specifies an end time.</span></span>
<span data-ttu-id="7ff3c-132">To polecenie cmdlet pobiera raporty o odbieranych wcześniej automatyzacjach.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="7ff3c-133">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="7ff3c-133">-Id</span></span>
<span data-ttu-id="7ff3c-134">Określa unikatowy identyfikator raportu węzła DSC dla tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="7ff3c-135">— najnowsza wersja</span><span class="sxs-lookup"><span data-stu-id="7ff3c-135">-Latest</span></span>
<span data-ttu-id="7ff3c-136">Wskazuje, że to polecenie cmdlet pobiera najnowszy raport DSC tylko dla określonego węzła.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="7ff3c-137">- NodeId</span><span class="sxs-lookup"><span data-stu-id="7ff3c-137">-NodeId</span></span>
<span data-ttu-id="7ff3c-138">Określa unikatowy identyfikator węzła DSC, dla którego to polecenie cmdlet pobiera raporty.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="7ff3c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ff3c-139">-ResourceGroupName</span></span>
<span data-ttu-id="7ff3c-140">Określa nazwę grupy zasobów zawierającej węzeł DSC, dla którego to polecenie cmdlet pobiera raporty.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="7ff3c-141">— StartTime</span><span class="sxs-lookup"><span data-stu-id="7ff3c-141">-StartTime</span></span>
<span data-ttu-id="7ff3c-142">Określa czas rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-142">Specifies a start time.</span></span>
<span data-ttu-id="7ff3c-143">To polecenie cmdlet pobiera raporty, które po tym czasie otrzymano automatyzację.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="7ff3c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff3c-144">CommonParameters</span></span>
<span data-ttu-id="7ff3c-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff3c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff3c-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ff3c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff3c-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ff3c-147">INPUTS</span></span>

### <span data-ttu-id="7ff3c-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7ff3c-148">System.Guid</span></span>

### <span data-ttu-id="7ff3c-149">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7ff3c-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7ff3c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7ff3c-150">System.String</span></span>

## <span data-ttu-id="7ff3c-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ff3c-151">OUTPUTS</span></span>

### <span data-ttu-id="7ff3c-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="7ff3c-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="7ff3c-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ff3c-153">NOTES</span></span>

## <span data-ttu-id="7ff3c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ff3c-154">RELATED LINKS</span></span>

[<span data-ttu-id="7ff3c-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7ff3c-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="7ff3c-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="7ff3c-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


