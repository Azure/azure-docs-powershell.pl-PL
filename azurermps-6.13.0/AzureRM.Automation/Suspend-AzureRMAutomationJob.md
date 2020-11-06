---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 0820905ff8a4673c9abae56be2f7792912095e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543947"
---
# <span data-ttu-id="eaffa-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="eaffa-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="eaffa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaffa-102">SYNOPSIS</span></span>
<span data-ttu-id="eaffa-103">Wstrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="eaffa-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaffa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaffa-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaffa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eaffa-105">DESCRIPTION</span></span>
<span data-ttu-id="eaffa-106">Polecenie cmdlet **Suspend-AzureRmAutomationJob** zawiesza zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="eaffa-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="eaffa-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="eaffa-107">Specify a running Automation job.</span></span>
<span data-ttu-id="eaffa-108">Aby wznowić zawieszone zadanie, użyj polecenia cmdlet Resume-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="eaffa-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="eaffa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaffa-109">EXAMPLES</span></span>

### <span data-ttu-id="eaffa-110">Przykład 1: Wstrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="eaffa-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eaffa-111">To polecenie zawiesza zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="eaffa-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="eaffa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaffa-112">PARAMETERS</span></span>

### <span data-ttu-id="eaffa-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eaffa-113">-AutomationAccountName</span></span>
<span data-ttu-id="eaffa-114">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet zawiesza zadanie.</span><span class="sxs-lookup"><span data-stu-id="eaffa-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="eaffa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaffa-115">-DefaultProfile</span></span>
<span data-ttu-id="eaffa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eaffa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaffa-117">-ID</span><span class="sxs-lookup"><span data-stu-id="eaffa-117">-Id</span></span>
<span data-ttu-id="eaffa-118">Określa identyfikator zadania zawieszanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaffa-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaffa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaffa-119">-ResourceGroupName</span></span>
<span data-ttu-id="eaffa-120">Określa identyfikator zadania zawieszanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaffa-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="eaffa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaffa-121">CommonParameters</span></span>
<span data-ttu-id="eaffa-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaffa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaffa-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaffa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaffa-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaffa-124">INPUTS</span></span>

### <span data-ttu-id="eaffa-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="eaffa-125">System.Guid</span></span>

### <span data-ttu-id="eaffa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="eaffa-126">System.String</span></span>

## <span data-ttu-id="eaffa-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaffa-127">OUTPUTS</span></span>

### <span data-ttu-id="eaffa-128">System. void</span><span class="sxs-lookup"><span data-stu-id="eaffa-128">System.Void</span></span>

## <span data-ttu-id="eaffa-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaffa-129">NOTES</span></span>

## <span data-ttu-id="eaffa-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaffa-130">RELATED LINKS</span></span>

[<span data-ttu-id="eaffa-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="eaffa-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="eaffa-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="eaffa-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="eaffa-133">Życiorys — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="eaffa-133">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="eaffa-134">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="eaffa-134">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


