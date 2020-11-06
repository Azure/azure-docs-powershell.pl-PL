---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: db7e76a21f635429be598ca9f40899ece3fa0406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552428"
---
# <span data-ttu-id="15444-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="15444-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="15444-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15444-102">SYNOPSIS</span></span>
<span data-ttu-id="15444-103">Zatrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="15444-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15444-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15444-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15444-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15444-105">DESCRIPTION</span></span>
<span data-ttu-id="15444-106">Polecenie cmdlet **stop-AzureRmAutomationJob** zatrzymuje zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="15444-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="15444-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="15444-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="15444-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15444-108">EXAMPLES</span></span>

### <span data-ttu-id="15444-109">Przykład 1: Zatrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="15444-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="15444-110">To polecenie zatrzymuje zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="15444-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="15444-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15444-111">PARAMETERS</span></span>

### <span data-ttu-id="15444-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="15444-112">-AutomationAccountName</span></span>
<span data-ttu-id="15444-113">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet zatrzymuje zadanie.</span><span class="sxs-lookup"><span data-stu-id="15444-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="15444-114">-ID</span><span class="sxs-lookup"><span data-stu-id="15444-114">-Id</span></span>
<span data-ttu-id="15444-115">Określa identyfikator zadania, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15444-115">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="15444-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15444-116">-ResourceGroupName</span></span>
<span data-ttu-id="15444-117">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15444-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="15444-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15444-118">-DefaultProfile</span></span>
<span data-ttu-id="15444-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15444-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15444-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15444-120">CommonParameters</span></span>
<span data-ttu-id="15444-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15444-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15444-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15444-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15444-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15444-123">INPUTS</span></span>

## <span data-ttu-id="15444-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15444-124">OUTPUTS</span></span>

## <span data-ttu-id="15444-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15444-125">NOTES</span></span>

## <span data-ttu-id="15444-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15444-126">RELATED LINKS</span></span>

[<span data-ttu-id="15444-127">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="15444-127">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="15444-128">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="15444-128">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="15444-129">Życiorys — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="15444-129">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="15444-130">Suspend — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="15444-130">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


