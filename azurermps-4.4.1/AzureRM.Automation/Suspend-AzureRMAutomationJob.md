---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: cc9f402400b0290d8cf36dc38d59a45e29ce770c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718743"
---
# <span data-ttu-id="c3286-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c3286-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="c3286-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3286-102">SYNOPSIS</span></span>
<span data-ttu-id="c3286-103">Wstrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c3286-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3286-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3286-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3286-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3286-105">DESCRIPTION</span></span>
<span data-ttu-id="c3286-106">Polecenie cmdlet **Suspend-AzureRmAutomationJob** zawiesza zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c3286-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="c3286-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c3286-107">Specify a running Automation job.</span></span>

<span data-ttu-id="c3286-108">Aby wznowić zawieszone zadanie, użyj polecenia cmdlet Resume-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="c3286-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="c3286-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3286-109">EXAMPLES</span></span>

### <span data-ttu-id="c3286-110">Przykład 1: Wstrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="c3286-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c3286-111">To polecenie zawiesza zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="c3286-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="c3286-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3286-112">PARAMETERS</span></span>

### <span data-ttu-id="c3286-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c3286-113">-AutomationAccountName</span></span>
<span data-ttu-id="c3286-114">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet zawiesza zadanie.</span><span class="sxs-lookup"><span data-stu-id="c3286-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="c3286-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c3286-115">-Id</span></span>
<span data-ttu-id="c3286-116">Określa identyfikator zadania zawieszanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3286-116">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="c3286-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3286-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3286-118">Określa identyfikator zadania zawieszanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3286-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="c3286-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3286-119">-DefaultProfile</span></span>
<span data-ttu-id="c3286-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3286-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3286-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3286-121">CommonParameters</span></span>
<span data-ttu-id="c3286-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3286-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3286-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3286-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3286-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3286-124">INPUTS</span></span>

## <span data-ttu-id="c3286-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3286-125">OUTPUTS</span></span>

## <span data-ttu-id="c3286-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3286-126">NOTES</span></span>

## <span data-ttu-id="c3286-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3286-127">RELATED LINKS</span></span>

[<span data-ttu-id="c3286-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c3286-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="c3286-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c3286-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="c3286-130">Życiorys — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c3286-130">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="c3286-131">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c3286-131">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


