---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719583"
---
# <span data-ttu-id="82ac5-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="82ac5-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="82ac5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="82ac5-103">Umożliwia pobieranie raportów wysłanych z węzła DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="82ac5-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ac5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82ac5-104">SYNTAX</span></span>

### <span data-ttu-id="82ac5-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="82ac5-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82ac5-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="82ac5-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82ac5-107">ById</span><span class="sxs-lookup"><span data-stu-id="82ac5-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ac5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="82ac5-108">DESCRIPTION</span></span>
<span data-ttu-id="82ac5-109">Polecenie cmdlet **Get-AzureRmAutomationDscNodeReport** pobiera raporty wysyłane z węzła APS (Konfiguracja stanu żądanego) do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="82ac5-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="82ac5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82ac5-110">EXAMPLES</span></span>

### <span data-ttu-id="82ac5-111">Przykład 1. pobieranie wszystkich raportów dla węzła DSC</span><span class="sxs-lookup"><span data-stu-id="82ac5-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="82ac5-112">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82ac5-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="82ac5-113">Polecenie zapisuje ten obiekt w zmiennej $Node.</span><span class="sxs-lookup"><span data-stu-id="82ac5-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="82ac5-114">Drugie polecenie pobiera metadane wszystkich raportów wysyłanych z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82ac5-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="82ac5-115">Polecenie określa węzeł za pomocą właściwości **Identyfikator** obiektu $Node.</span><span class="sxs-lookup"><span data-stu-id="82ac5-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="82ac5-116">Przykład 2: uzyskiwanie raportu dla węzła DSC według identyfikatora raportu</span><span class="sxs-lookup"><span data-stu-id="82ac5-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="82ac5-117">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82ac5-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="82ac5-118">Polecenie zapisuje ten obiekt w zmiennej $Node.</span><span class="sxs-lookup"><span data-stu-id="82ac5-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="82ac5-119">Drugie polecenie pobiera metadane dla raportu określonego IDENTYFIKATORem wysłanym z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82ac5-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="82ac5-120">Przykład 3: uzyskiwanie najnowszego raportu dla węzła DSC</span><span class="sxs-lookup"><span data-stu-id="82ac5-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="82ac5-121">Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82ac5-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="82ac5-122">Polecenie zapisuje ten obiekt w zmiennej $Node.</span><span class="sxs-lookup"><span data-stu-id="82ac5-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="82ac5-123">Drugie polecenie pobiera metadane najnowszego raportu wysłanego z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82ac5-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="82ac5-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82ac5-124">PARAMETERS</span></span>

### <span data-ttu-id="82ac5-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82ac5-125">-AutomationAccountName</span></span>
<span data-ttu-id="82ac5-126">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="82ac5-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="82ac5-127">To polecenie cmdlet powoduje wyeksportowanie raportów dla węzła DSC należącego do konta, które jest określone przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="82ac5-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="82ac5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ac5-128">-DefaultProfile</span></span>
<span data-ttu-id="82ac5-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="82ac5-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82ac5-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="82ac5-130">-EndTime</span></span>
<span data-ttu-id="82ac5-131">Określa godzinę zakończenia.</span><span class="sxs-lookup"><span data-stu-id="82ac5-131">Specifies an end time.</span></span>
<span data-ttu-id="82ac5-132">To polecenie cmdlet umożliwia pobieranie raportów, które zostały odebrane przed upływem tego czasu.</span><span class="sxs-lookup"><span data-stu-id="82ac5-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ac5-133">-ID</span><span class="sxs-lookup"><span data-stu-id="82ac5-133">-Id</span></span>
<span data-ttu-id="82ac5-134">Określa unikatowy identyfikator raportu węzła DSC dla tego polecenia cmdlet, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="82ac5-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ac5-135">-Najnowsze</span><span class="sxs-lookup"><span data-stu-id="82ac5-135">-Latest</span></span>
<span data-ttu-id="82ac5-136">Wskazuje, że ten aplet polecenia pobiera najnowszy raport DSC tylko dla określonego węzła.</span><span class="sxs-lookup"><span data-stu-id="82ac5-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByLatest
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ac5-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="82ac5-137">-NodeId</span></span>
<span data-ttu-id="82ac5-138">Określa unikatowy identyfikator węzła DSC, dla którego ten aplet polecenia pobiera raporty.</span><span class="sxs-lookup"><span data-stu-id="82ac5-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ac5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ac5-139">-ResourceGroupName</span></span>
<span data-ttu-id="82ac5-140">Określa nazwę grupy zasobów zawierającej węzeł DSC, dla którego ten aplet polecenia pobiera raporty.</span><span class="sxs-lookup"><span data-stu-id="82ac5-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="82ac5-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="82ac5-141">-StartTime</span></span>
<span data-ttu-id="82ac5-142">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="82ac5-142">Specifies a start time.</span></span>
<span data-ttu-id="82ac5-143">To polecenie cmdlet umożliwia pobieranie raportów, które zostały odebrane po upływie tego czasu.</span><span class="sxs-lookup"><span data-stu-id="82ac5-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ac5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ac5-144">CommonParameters</span></span>
<span data-ttu-id="82ac5-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ac5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ac5-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ac5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ac5-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82ac5-147">INPUTS</span></span>

### <span data-ttu-id="82ac5-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="82ac5-148">None</span></span>
<span data-ttu-id="82ac5-149">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="82ac5-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82ac5-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82ac5-150">OUTPUTS</span></span>

### <span data-ttu-id="82ac5-151">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="82ac5-151">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="82ac5-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82ac5-152">NOTES</span></span>

## <span data-ttu-id="82ac5-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82ac5-153">RELATED LINKS</span></span>

[<span data-ttu-id="82ac5-154">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="82ac5-154">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="82ac5-155">Eksportowanie — AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="82ac5-155">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


