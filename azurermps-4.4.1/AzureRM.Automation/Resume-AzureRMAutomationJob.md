---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 6d23fe3728b569cbb1a2aee498d560672ee75877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547084"
---
# <span data-ttu-id="3a572-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a572-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="3a572-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a572-102">SYNOPSIS</span></span>
<span data-ttu-id="3a572-103">Wznawia zawieszone zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3a572-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a572-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a572-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a572-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a572-105">DESCRIPTION</span></span>
<span data-ttu-id="3a572-106">Polecenie cmdlet **Resume-AzureRmAutomationJob** Wznawia zawieszone zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3a572-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="3a572-107">Określ zawieszone zadanie.</span><span class="sxs-lookup"><span data-stu-id="3a572-107">Specify the suspended job.</span></span>

<span data-ttu-id="3a572-108">Aby zawiesić zadanie, użyj polecenia cmdlet Suspend-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="3a572-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="3a572-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a572-109">EXAMPLES</span></span>

### <span data-ttu-id="3a572-110">Przykład 1: wznawianie zawieszonego zadania</span><span class="sxs-lookup"><span data-stu-id="3a572-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3a572-111">To polecenie wznawia zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="3a572-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="3a572-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a572-112">PARAMETERS</span></span>

### <span data-ttu-id="3a572-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a572-113">-AutomationAccountName</span></span>
<span data-ttu-id="3a572-114">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet wznawia zadanie.</span><span class="sxs-lookup"><span data-stu-id="3a572-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="3a572-115">-ID</span><span class="sxs-lookup"><span data-stu-id="3a572-115">-Id</span></span>
<span data-ttu-id="3a572-116">Określa identyfikator zadania, które zostanie wznowione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a572-116">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="3a572-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a572-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a572-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet wznawia zadanie.</span><span class="sxs-lookup"><span data-stu-id="3a572-118">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="3a572-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a572-119">-DefaultProfile</span></span>
<span data-ttu-id="3a572-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a572-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a572-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a572-121">CommonParameters</span></span>
<span data-ttu-id="3a572-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a572-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a572-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a572-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a572-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a572-124">INPUTS</span></span>

## <span data-ttu-id="3a572-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a572-125">OUTPUTS</span></span>

## <span data-ttu-id="3a572-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a572-126">NOTES</span></span>

## <span data-ttu-id="3a572-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a572-127">RELATED LINKS</span></span>

[<span data-ttu-id="3a572-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a572-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="3a572-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="3a572-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="3a572-130">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a572-130">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="3a572-131">Suspend — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a572-131">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


