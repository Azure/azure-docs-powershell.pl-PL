---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182170"
---
# <span data-ttu-id="652fd-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="652fd-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="652fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="652fd-102">SYNOPSIS</span></span>
<span data-ttu-id="652fd-103">Pobiera hybrydowe grupy pracowników podręcznika.</span><span class="sxs-lookup"><span data-stu-id="652fd-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="652fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="652fd-104">SYNTAX</span></span>

### <span data-ttu-id="652fd-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="652fd-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="652fd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="652fd-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="652fd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="652fd-107">DESCRIPTION</span></span>
<span data-ttu-id="652fd-108">Polecenie **cmdlet Get-AzAutomationHybridWorkerGroup** pobiera grupy pracowników hybrydowego podręcznika azure Automation.</span><span class="sxs-lookup"><span data-stu-id="652fd-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="652fd-109">Aby uzyskać określoną grupę, określ jej nazwę.</span><span class="sxs-lookup"><span data-stu-id="652fd-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="652fd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="652fd-110">EXAMPLES</span></span>

### <span data-ttu-id="652fd-111">Przykład 1. Pobierz wszystkie hybrydowe grupy pracowników podręcznika</span><span class="sxs-lookup"><span data-stu-id="652fd-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="652fd-112">To polecenie pobiera wszystkie grupy pracowników hybrydowego podręcznika obsługi na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="652fd-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="652fd-113">Przykład 2. Uzyskiwanie jednej grupy pracowników hybrydowego podręcznika uruchamiania</span><span class="sxs-lookup"><span data-stu-id="652fd-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="652fd-114">To polecenie pobiera grupę pracowników hybrydowego podręcznika o nazwie HybridRunbookWorkerGroup01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="652fd-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="652fd-115">Przykład 3. Uzyskiwanie pracowników w grupie pracowników hybrydowego podręcznika</span><span class="sxs-lookup"><span data-stu-id="652fd-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="652fd-116">To polecenie pobiera pracowników hybrydowego podręcznika w grupie pracowników hybrydowego podręcznika o nazwie HybridRunbookWorkerGroup01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="652fd-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="652fd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="652fd-117">PARAMETERS</span></span>

### <span data-ttu-id="652fd-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="652fd-118">-AutomationAccountName</span></span>
<span data-ttu-id="652fd-119">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="652fd-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="652fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="652fd-120">-DefaultProfile</span></span>
<span data-ttu-id="652fd-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="652fd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="652fd-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="652fd-122">-Name</span></span>
<span data-ttu-id="652fd-123">Określa nazwę grupy hybrydowego pracownika podręcznika.</span><span class="sxs-lookup"><span data-stu-id="652fd-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="652fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="652fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="652fd-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="652fd-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="652fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="652fd-126">CommonParameters</span></span>
<span data-ttu-id="652fd-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="652fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="652fd-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="652fd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="652fd-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="652fd-129">INPUTS</span></span>

### <span data-ttu-id="652fd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="652fd-130">System.String</span></span>

## <span data-ttu-id="652fd-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="652fd-131">OUTPUTS</span></span>

### <span data-ttu-id="652fd-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="652fd-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="652fd-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="652fd-133">NOTES</span></span>

## <span data-ttu-id="652fd-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="652fd-134">RELATED LINKS</span></span>
