---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 8e84f2f66703410b626769be8c2c2d5a57e531e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541979"
---
# <span data-ttu-id="0d503-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0d503-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="0d503-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d503-102">SYNOPSIS</span></span>
<span data-ttu-id="0d503-103">Wznawia zawieszone zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="0d503-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d503-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d503-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d503-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d503-105">DESCRIPTION</span></span>
<span data-ttu-id="0d503-106">Polecenie cmdlet **Resume-AzureRmAutomationJob** Wznawia zawieszone zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0d503-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="0d503-107">Określ zawieszone zadanie.</span><span class="sxs-lookup"><span data-stu-id="0d503-107">Specify the suspended job.</span></span>
<span data-ttu-id="0d503-108">Aby zawiesić zadanie, użyj polecenia cmdlet Suspend-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="0d503-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="0d503-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d503-109">EXAMPLES</span></span>

### <span data-ttu-id="0d503-110">Przykład 1: wznawianie zawieszonego zadania</span><span class="sxs-lookup"><span data-stu-id="0d503-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0d503-111">To polecenie wznawia zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="0d503-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="0d503-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d503-112">PARAMETERS</span></span>

### <span data-ttu-id="0d503-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0d503-113">-AutomationAccountName</span></span>
<span data-ttu-id="0d503-114">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet wznawia zadanie.</span><span class="sxs-lookup"><span data-stu-id="0d503-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="0d503-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d503-115">-DefaultProfile</span></span>
<span data-ttu-id="0d503-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0d503-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d503-117">-ID</span><span class="sxs-lookup"><span data-stu-id="0d503-117">-Id</span></span>
<span data-ttu-id="0d503-118">Określa identyfikator zadania, które zostanie wznowione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d503-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="0d503-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d503-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d503-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet wznawia zadanie.</span><span class="sxs-lookup"><span data-stu-id="0d503-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="0d503-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d503-121">CommonParameters</span></span>
<span data-ttu-id="0d503-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d503-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d503-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d503-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d503-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d503-124">INPUTS</span></span>

### <span data-ttu-id="0d503-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0d503-125">System.Guid</span></span>

### <span data-ttu-id="0d503-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0d503-126">System.String</span></span>

## <span data-ttu-id="0d503-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d503-127">OUTPUTS</span></span>

### <span data-ttu-id="0d503-128">System. void</span><span class="sxs-lookup"><span data-stu-id="0d503-128">System.Void</span></span>

## <span data-ttu-id="0d503-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d503-129">NOTES</span></span>

## <span data-ttu-id="0d503-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d503-130">RELATED LINKS</span></span>

[<span data-ttu-id="0d503-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0d503-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="0d503-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="0d503-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="0d503-133">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0d503-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="0d503-134">Suspend — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0d503-134">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


